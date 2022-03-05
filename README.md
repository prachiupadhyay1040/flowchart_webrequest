# flowchart_webrequest
graphviz flowchart on web request

digraph G {


    node [shape=rectangle,style=filled,fontname = "Handlee"];
    edge [fontname = "Handlee"];
     
    start [
    label = "start";
    shape = oval;];
    
    web [
    label = "Web browser";
    shape = rec;];
    
    URL [
    label = "Enter URL";
    shape = rec;];
    
    status [
    label = "Status Code";
    shape = rec;];
    
    DNS [
    label = "DNS Server 
    search for cache";
    shape = diamond;];
    
    IP [
    label = "IP Address obtained";
    shape = rec;];
    
    HTTP[
    label = "HTTP request to web server 
    using TCP or IP";
    shape = rec;];
    
    Host[
    label = "Host computer receive 
    HTTP request & send back response";
    shape = rec;];
    
    render[
    label = "Browser renders the response";
    shape = rec;];
    
    Packet[
    label = "Each HTTP response inside 
    have another IP Packet";
    shape = rec;];
    
    display[
    label = "Browser displays HTML Content";
    shape = rec;];
    
    end[
    label = "end";
    shape = oval;];
    
    q[
    label = "abc";
        shape = rec;];
    
                
 start -> web;
 web -> URL;
 URL -> status;
 status-> DNS;
 DNS -> q[label="No"];
 {rank=same;
    DNS; q;
 }
 DNS:s -> IP[label="yes"];
 IP -> HTTP;
HTTP -> Host;
Host -> render;
render -> Packet;
Packet -> display;
display -> end;

}

https://dreampuf.github.io/GraphvizOnline/#digraph%20G%20%7B%0A%0A%0A%20%20%20%20node%20%5Bshape%3Drectangle%2Cstyle%3Dfilled%2Cfontname%20%3D%20%22Handlee%22%5D%3B%0A%20%20%20%20edge%20%5Bfontname%20%3D%20%22Handlee%22%5D%3B%0A%20%20%20%20%20%0A%20%20%20%20start%20%5B%0A%20%20%20%20label%20%3D%20%22start%22%3B%0A%20%20%20%20shape%20%3D%20oval%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20web%20%5B%0A%20%20%20%20label%20%3D%20%22Web%20browser%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20URL%20%5B%0A%20%20%20%20label%20%3D%20%22Enter%20URL%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20status%20%5B%0A%20%20%20%20label%20%3D%20%22Status%20Code%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20DNS%20%5B%0A%20%20%20%20label%20%3D%20%22DNS%20Server%20%0A%20%20%20%20search%20for%20cache%22%3B%0A%20%20%20%20shape%20%3D%20diamond%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20IP%20%5B%0A%20%20%20%20label%20%3D%20%22IP%20Address%20obtained%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20HTTP%5B%0A%20%20%20%20label%20%3D%20%22HTTP%20request%20to%20web%20server%20%0A%20%20%20%20using%20TCP%20or%20IP%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20Host%5B%0A%20%20%20%20label%20%3D%20%22Host%20computer%20receive%20%0A%20%20%20%20HTTP%20request%20%26%20send%20back%20response%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20render%5B%0A%20%20%20%20label%20%3D%20%22Browser%20renders%20the%20response%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20Packet%5B%0A%20%20%20%20label%20%3D%20%22Each%20HTTP%20response%20inside%20%0A%20%20%20%20have%20another%20IP%20Packet%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20display%5B%0A%20%20%20%20label%20%3D%20%22Browser%20displays%20HTML%20Content%22%3B%0A%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20end%5B%0A%20%20%20%20label%20%3D%20%22end%22%3B%0A%20%20%20%20shape%20%3D%20oval%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20q%5B%0A%20%20%20%20%20%20%20%20label%20%3D%20%22abc%22%3B%0A%20%20%20%20%20%20%20%20shape%20%3D%20rec%3B%5D%3B%0A%20%20%20%20%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%0A%20start%20-%3E%20web%3B%0A%20web%20-%3E%20URL%3B%0A%20URL%20-%3E%20status%3B%0A%20status-%3E%20DNS%3B%0A%20DNS%20-%3E%20q%5Blabel%3D%22No%22%5D%3B%0A%20%7Brank%3Dsame%3B%0A%20%20%20%20DNS%3B%20q%3B%0A%20%7D%0A%20DNS%3As%20-%3E%20IP%5Blabel%3D%22yes%22%5D%3B%0A%20IP%20-%3E%20HTTP%3B%0AHTTP%20-%3E%20Host%3B%0AHost%20-%3E%20render%3B%0Arender%20-%3E%20Packet%3B%0APacket%20-%3E%20display%3B%0Adisplay%20-%3E%20end%3B%0A%0A%7D%0A
