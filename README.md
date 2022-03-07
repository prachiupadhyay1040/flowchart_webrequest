# flowchart_webrequest

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
start -> web; web -> URL; URL -> status; status-> DNS; DNS -> q[label="No"]; {rank=same; DNS; q; } DNS:s -> IP[label="yes"]; IP -> HTTP; HTTP -> Host; Host -> render; render -> Packet; Packet -> display; display -> end;

}
