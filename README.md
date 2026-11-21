
function formatText(text){
 let safe=text
  .replaceAll("&","&amp;")
  .replaceAll("<","&lt;")
  .replaceAll(">","&gt;");

 const connectors=[
  "HOWEVER","THEREFORE","BECAUSE",
  "ALTHOUGH","WHILE","AND","BUT","SO"
 ];

 connectors.forEach(word=>{
  const regex=new RegExp("\\b"+word+"\\b","gi");
  safe=safe.replace(regex,"<strong>"+word+"</strong>");
 });

 const timePrepositions=[
  "ON","IN","AT","DURING","AFTER","BEFORE"
 ];

 timePrepositions.forEach(word=>{
  const regex=new RegExp(
   "\\b"+word+"\\b(?=\\s+(?:January|February|March|April|May|June|July|August|September|October|November|December|1910|1911|1913|1914|1917|the twentieth century|the uprising|the government|the revolution))",
   "gi"
  );
  safe=safe.replace(regex,"<u>$&</u>");
 });

 return safe;
}
