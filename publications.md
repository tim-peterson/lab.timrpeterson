---
layout: page
title: Publications
permalink: /publications/
---



<div style="display: inline-block;position: relative;width: 100%;">
<div style="margin-top:100%"></div>
<iframe style="    background-position:center center;
    background-repeat: no-repeat;
    background-size:100% 100%;
    height:100%;
    width:100%;
    background-size: cover;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;border: 1px solid rgb(229,229,229);
    padding: 0.25rem;
    border-radius: 3px;" src="https://www.ncbi.nlm.nih.gov/pubmed/?term=Peterson%20TR%5BAuthor%5D&cauthor=true&cauthor_uid=23202129"></iframe>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script>
//http://www.alexhadik.com/blog/2014/6/12/create-pubmed-citations-automatically-using-pubmed-api
function iterateJSON(idlist, publications) {

    var id = idlist.pop();
    $.getJSON('http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id='+id+'&retmode=json', function(summary){

        var citation = "";
        
        for(author in summary.result[id].authors){
            citation+=summary.result[id].authors[author].name+', ';
        }
        citation+=' \"'+summary.result[id].title+'\" <i>'+summary.result[id].fulljournalname+'</i> '+summary.result[id].volume+'.'+summary.result[id].issue+' ('+summary.result[id].pubdate+'): '+summary.result[id].pages+'.';
        
        console.log(citation);
        publications.push(citation);
        
        if(idlist.length!=0){
            iterateJSON(idlist, publications);
        }else{
            console.log(publications);
        }
                
    });
}

$.getJSON('http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=peterson+tr[author]&retmode=json', function(data){
    var ids = data.esearchresult.idlist;
    var publications = [];
    iterateJSON(ids, publications);
});

</script>




