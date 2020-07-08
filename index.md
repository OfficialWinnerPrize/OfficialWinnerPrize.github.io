



<!doctype html>
<html lang="en">
<head>
    <!-- Meta tags -->
    <meta charset="utf-8"><script type="text/javascript">(window.NREUM||(NREUM={})).loader_config={xpid:"UgQAU1JbGwACVlVTBwk=",licenseKey:"cf1f842459",applicationID:"3224108"};window.NREUM||(NREUM={}),__nr_require=function(t,n,e){function r(e){if(!n[e]){var o=n[e]={exports:{}};t[e][0].call(o.exports,function(n){var o=t[e][1][n];return r(o||n)},o,o.exports)}return n[e].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<e.length;o++)r(e[o]);return r}({1:[function(t,n,e){function r(t){try{s.console&&console.log(t)}catch(n){}}var o,i=t("ee"),a=t(21),s={};try{o=localStorage.getItem("__nr_flags").split(","),console&&"function"==typeof console.log&&(s.console=!0,o.indexOf("dev")!==-1&&(s.dev=!0),o.indexOf("nr_dev")!==-1&&(s.nrDev=!0))}catch(c){}s.nrDev&&i.on("internal-error",function(t){r(t.stack)}),s.dev&&i.on("fn-err",function(t,n,e){r(e.stack)}),s.dev&&(r("NR AGENT IN DEVELOPMENT MODE"),r("flags: "+a(s,function(t,n){return t}).join(", ")))},{}],2:[function(t,n,e){function r(t,n,e,r,s){try{p?p-=1:o(s||new UncaughtException(t,n,e),!0)}catch(f){try{i("ierr",[f,c.now(),!0])}catch(d){}}return"function"==typeof u&&u.apply(this,a(arguments))}function UncaughtException(t,n,e){this.message=t||"Uncaught error with no additional information",this.sourceURL=n,this.line=e}function o(t,n){var e=n?null:c.now();i("err",[t,e])}var i=t("handle"),a=t(22),s=t("ee"),c=t("loader"),f=t("gos"),u=window.onerror,d=!1,l="nr@seenError",p=0;c.features.err=!0,t(1),window.onerror=r;try{throw new Error}catch(h){"stack"in h&&(t(9),t(8),"addEventListener"in window&&t(5),c.xhrWrappable&&t(10),d=!0)}s.on("fn-start",function(t,n,e){d&&(p+=1)}),s.on("fn-err",function(t,n,e){d&&!e[l]&&(f(e,l,function(){return!0}),this.thrown=!0,o(e))}),s.on("fn-end",function(){d&&!this.thrown&&p>0&&(p-=1)}),s.on("internal-error",function(t){i("ierr",[t,c.now(),!0])})},{}],3:[function(t,n,e){t("loader").features.ins=!0},{}],4:[function(t,n,e){function r(t){}if(window.performance&&window.performance.timing&&window.performance.getEntriesByType){var o=t("ee"),i=t("handle"),a=t(9),s=t(8),c="learResourceTimings",f="addEventListener",u="resourcetimingbufferfull",d="bstResource",l="resource",p="-start",h="-end",m="fn"+p,w="fn"+h,v="bstTimer",g="pushState",y=t("loader");y.features.stn=!0,t(7),"addEventListener"in window&&t(5);var x=NREUM.o.EV;o.on(m,function(t,n){var e=t[0];e instanceof x&&(this.bstStart=y.now())}),o.on(w,function(t,n){var e=t[0];e instanceof x&&i("bst",[e,n,this.bstStart,y.now()])}),a.on(m,function(t,n,e){this.bstStart=y.now(),this.bstType=e}),a.on(w,function(t,n){i(v,[n,this.bstStart,y.now(),this.bstType])}),s.on(m,function(){this.bstStart=y.now()}),s.on(w,function(t,n){i(v,[n,this.bstStart,y.now(),"requestAnimationFrame"])}),o.on(g+p,function(t){this.time=y.now(),this.startPath=location.pathname+location.hash}),o.on(g+h,function(t){i("bstHist",[location.pathname+location.hash,this.startPath,this.time])}),f in window.performance&&(window.performance["c"+c]?window.performance[f](u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["c"+c]()},!1):window.performance[f]("webkit"+u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["webkitC"+c]()},!1)),document[f]("scroll",r,{passive:!0}),document[f]("keypress",r,!1),document[f]("click",r,!1)}},{}],5:[function(t,n,e){function r(t){for(var n=t;n&&!n.hasOwnProperty(u);)n=Object.getPrototypeOf(n);n&&o(n)}function o(t){s.inPlace(t,[u,d],"-",i)}function i(t,n){return t[1]}var a=t("ee").get("events"),s=t("wrap-function")(a,!0),c=t("gos"),f=XMLHttpRequest,u="addEventListener",d="removeEventListener";n.exports=a,"getPrototypeOf"in Object?(r(document),r(window),r(f.prototype)):f.prototype.hasOwnProperty(u)&&(o(window),o(f.prototype)),a.on(u+"-start",function(t,n){var e=t[1],r=c(e,"nr@wrapped",function(){function t(){if("function"==typeof e.handleEvent)return e.handleEvent.apply(e,arguments)}var n={object:t,"function":e}[typeof e];return n?s(n,"fn-",null,n.name||"anonymous"):e});this.wrapped=t[1]=r}),a.on(d+"-start",function(t){t[1]=this.wrapped||t[1]})},{}],6:[function(t,n,e){function r(t,n,e){var r=t[n];"function"==typeof r&&(t[n]=function(){var t=i(arguments),n={};o.emit(e+"before-start",[t],n);var a;n[m]&&n[m].dt&&(a=n[m].dt);var s=r.apply(this,t);return o.emit(e+"start",[t,a],s),s.then(function(t){return o.emit(e+"end",[null,t],s),t},function(t){throw o.emit(e+"end",[t],s),t})})}var o=t("ee").get("fetch"),i=t(22),a=t(21);n.exports=o;var s=window,c="fetch-",f=c+"body-",u=["arrayBuffer","blob","json","text","formData"],d=s.Request,l=s.Response,p=s.fetch,h="prototype",m="nr@context";d&&l&&p&&(a(u,function(t,n){r(d[h],n,f),r(l[h],n,f)}),r(s,"fetch",c),o.on(c+"end",function(t,n){var e=this;if(n){var r=n.headers.get("content-length");null!==r&&(e.rxSize=r),o.emit(c+"done",[null,n],e)}else o.emit(c+"done",[t],e)}))},{}],7:[function(t,n,e){var r=t("ee").get("history"),o=t("wrap-function")(r);n.exports=r;var i=window.history&&window.history.constructor&&window.history.constructor.prototype,a=window.history;i&&i.pushState&&i.replaceState&&(a=i),o.inPlace(a,["pushState","replaceState"],"-")},{}],8:[function(t,n,e){var r=t("ee").get("raf"),o=t("wrap-function")(r),i="equestAnimationFrame";n.exports=r,o.inPlace(window,["r"+i,"mozR"+i,"webkitR"+i,"msR"+i],"raf-"),r.on("raf-start",function(t){t[0]=o(t[0],"fn-")})},{}],9:[function(t,n,e){function r(t,n,e){t[0]=a(t[0],"fn-",null,e)}function o(t,n,e){this.method=e,this.timerDuration=isNaN(t[1])?0:+t[1],t[0]=a(t[0],"fn-",this,e)}var i=t("ee").get("timer"),a=t("wrap-function")(i),s="setTimeout",c="setInterval",f="clearTimeout",u="-start",d="-";n.exports=i,a.inPlace(window,[s,"setImmediate"],s+d),a.inPlace(window,[c],c+d),a.inPlace(window,[f,"clearImmediate"],f+d),i.on(c+u,r),i.on(s+u,o)},{}],10:[function(t,n,e){function r(t,n){d.inPlace(n,["onreadystatechange"],"fn-",s)}function o(){var t=this,n=u.context(t);t.readyState>3&&!n.resolved&&(n.resolved=!0,u.emit("xhr-resolved",[],t)),d.inPlace(t,g,"fn-",s)}function i(t){y.push(t),h&&(b?b.then(a):w?w(a):(E=-E,O.data=E))}function a(){for(var t=0;t<y.length;t++)r([],y[t]);y.length&&(y=[])}function s(t,n){return n}function c(t,n){for(var e in t)n[e]=t[e];return n}t(5);var f=t("ee"),u=f.get("xhr"),d=t("wrap-function")(u),l=NREUM.o,p=l.XHR,h=l.MO,m=l.PR,w=l.SI,v="readystatechange",g=["onload","onerror","onabort","onloadstart","onloadend","onprogress","ontimeout"],y=[];n.exports=u;var x=window.XMLHttpRequest=function(t){var n=new p(t);try{u.emit("new-xhr",[n],n),n.addEventListener(v,o,!1)}catch(e){try{u.emit("internal-error",[e])}catch(r){}}return n};if(c(p,x),x.prototype=p.prototype,d.inPlace(x.prototype,["open","send"],"-xhr-",s),u.on("send-xhr-start",function(t,n){r(t,n),i(n)}),u.on("open-xhr-start",r),h){var b=m&&m.resolve();if(!w&&!m){var E=1,O=document.createTextNode(E);new h(a).observe(O,{characterData:!0})}}else f.on("fn-end",function(t){t[0]&&t[0].type===v||a()})},{}],11:[function(t,n,e){function r(t){if(!i(t))return null;var n=window.NREUM;if(!n.loader_config)return null;var e=(n.loader_config.accountID||"").toString()||null,r=(n.loader_config.agentID||"").toString()||null,s=(n.loader_config.trustKey||"").toString()||null;if(!e||!r)return null;var c=a.generateCatId(),f=a.generateCatId(),u=Date.now(),d=o(c,f,u,e,r,s);return{header:d,guid:c,traceId:f,timestamp:u}}function o(t,n,e,r,o,i){var a="btoa"in window&&"function"==typeof window.btoa;if(!a)return null;var s={v:[0,1],d:{ty:"Browser",ac:r,ap:o,id:t,tr:n,ti:e}};return i&&r!==i&&(s.d.tk=i),btoa(JSON.stringify(s))}function i(t){var n=!1,e=!1,r={};if("init"in NREUM&&"distributed_tracing"in NREUM.init&&(r=NREUM.init.distributed_tracing,e=!!r.enabled),e)if(t.sameOrigin)n=!0;else if(r.allowed_origins instanceof Array)for(var o=0;o<r.allowed_origins.length;o++){var i=s(r.allowed_origins[o]);if(t.hostname===i.hostname&&t.protocol===i.protocol&&t.port===i.port){n=!0;break}}return e&&n}var a=t(19),s=t(13);n.exports={generateTracePayload:r,shouldGenerateTrace:i}},{}],12:[function(t,n,e){function r(t){var n=this.params,e=this.metrics;if(!this.ended){this.ended=!0;for(var r=0;r<l;r++)t.removeEventListener(d[r],this.listener,!1);n.aborted||(e.duration=a.now()-this.startTime,this.loadCaptureCalled||4!==t.readyState?null==n.status&&(n.status=0):i(this,t),e.cbTime=this.cbTime,u.emit("xhr-done",[t],t),s("xhr",[n,e,this.startTime]))}}function o(t,n){var e=c(n),r=t.params;r.host=e.hostname+":"+e.port,r.pathname=e.pathname,t.parsedOrigin=c(n),t.sameOrigin=t.parsedOrigin.sameOrigin}function i(t,n){t.params.status=n.status;var e=w(n,t.lastSize);if(e&&(t.metrics.rxSize=e),t.sameOrigin){var r=n.getResponseHeader("X-NewRelic-App-Data");r&&(t.params.cat=r.split(", ").pop())}t.loadCaptureCalled=!0}var a=t("loader");if(a.xhrWrappable){var s=t("handle"),c=t(13),f=t(11).generateTracePayload,u=t("ee"),d=["load","error","abort","timeout"],l=d.length,p=t("id"),h=t(17),m=t(16),w=t(14),v=window.XMLHttpRequest;a.features.xhr=!0,t(10),t(6),u.on("new-xhr",function(t){var n=this;n.totalCbs=0,n.called=0,n.cbTime=0,n.end=r,n.ended=!1,n.xhrGuids={},n.lastSize=null,n.loadCaptureCalled=!1,t.addEventListener("load",function(e){i(n,t)},!1),h&&(h>34||h<10)||window.opera||t.addEventListener("progress",function(t){n.lastSize=t.loaded},!1)}),u.on("open-xhr-start",function(t){this.params={method:t[0]},o(this,t[1]),this.metrics={}}),u.on("open-xhr-end",function(t,n){"loader_config"in NREUM&&"xpid"in NREUM.loader_config&&this.sameOrigin&&n.setRequestHeader("X-NewRelic-ID",NREUM.loader_config.xpid);var e=f(this.parsedOrigin);e&&e.header&&(n.setRequestHeader("newrelic",e.header),this.dt=e)}),u.on("send-xhr-start",function(t,n){var e=this.metrics,r=t[0],o=this;if(e&&r){var i=m(r);i&&(e.txSize=i)}this.startTime=a.now(),this.listener=function(t){try{"abort"!==t.type||o.loadCaptureCalled||(o.params.aborted=!0),("load"!==t.type||o.called===o.totalCbs&&(o.onloadCalled||"function"!=typeof n.onload))&&o.end(n)}catch(e){try{u.emit("internal-error",[e])}catch(r){}}};for(var s=0;s<l;s++)n.addEventListener(d[s],this.listener,!1)}),u.on("xhr-cb-time",function(t,n,e){this.cbTime+=t,n?this.onloadCalled=!0:this.called+=1,this.called!==this.totalCbs||!this.onloadCalled&&"function"==typeof e.onload||this.end(e)}),u.on("xhr-load-added",function(t,n){var e=""+p(t)+!!n;this.xhrGuids&&!this.xhrGuids[e]&&(this.xhrGuids[e]=!0,this.totalCbs+=1)}),u.on("xhr-load-removed",function(t,n){var e=""+p(t)+!!n;this.xhrGuids&&this.xhrGuids[e]&&(delete this.xhrGuids[e],this.totalCbs-=1)}),u.on("addEventListener-end",function(t,n){n instanceof v&&"load"===t[0]&&u.emit("xhr-load-added",[t[1],t[2]],n)}),u.on("removeEventListener-end",function(t,n){n instanceof v&&"load"===t[0]&&u.emit("xhr-load-removed",[t[1],t[2]],n)}),u.on("fn-start",function(t,n,e){n instanceof v&&("onload"===e&&(this.onload=!0),("load"===(t[0]&&t[0].type)||this.onload)&&(this.xhrCbStart=a.now()))}),u.on("fn-end",function(t,n){this.xhrCbStart&&u.emit("xhr-cb-time",[a.now()-this.xhrCbStart,this.onload,n],n)}),u.on("fetch-before-start",function(t){var n,e=t[1]||{};"string"==typeof t[0]?n=t[0]:t[0]&&t[0].url&&(n=t[0].url),n&&(this.parsedOrigin=c(n),this.sameOrigin=this.parsedOrigin.sameOrigin);var r=f(this.parsedOrigin);if(r&&r.header){var o=r.header;if("string"==typeof t[0]){var i={};for(var a in e)i[a]=e[a];i.headers=new Headers(e.headers||{}),i.headers.set("newrelic",o),this.dt=r,t.length>1?t[1]=i:t.push(i)}else t[0]&&t[0].headers&&(t[0].headers.append("newrelic",o),this.dt=r)}})}},{}],13:[function(t,n,e){var r={};n.exports=function(t){if(t in r)return r[t];var n=document.createElement("a"),e=window.location,o={};n.href=t,o.port=n.port;var i=n.href.split("://");!o.port&&i[1]&&(o.port=i[1].split("/")[0].split("@").pop().split(":")[1]),o.port&&"0"!==o.port||(o.port="https"===i[0]?"443":"80"),o.hostname=n.hostname||e.hostname,o.pathname=n.pathname,o.protocol=i[0],"/"!==o.pathname.charAt(0)&&(o.pathname="/"+o.pathname);var a=!n.protocol||":"===n.protocol||n.protocol===e.protocol,s=n.hostname===document.domain&&n.port===e.port;return o.sameOrigin=a&&(!n.hostname||s),"/"===o.pathname&&(r[t]=o),o}},{}],14:[function(t,n,e){function r(t,n){var e=t.responseType;return"json"===e&&null!==n?n:"arraybuffer"===e||"blob"===e||"json"===e?o(t.response):"text"===e||"document"===e||""===e||void 0===e?o(t.responseText):void 0}var o=t(16);n.exports=r},{}],15:[function(t,n,e){function r(){}function o(t,n,e){return function(){return i(t,[f.now()].concat(s(arguments)),n?null:this,e),n?void 0:this}}var i=t("handle"),a=t(21),s=t(22),c=t("ee").get("tracer"),f=t("loader"),u=NREUM;"undefined"==typeof window.newrelic&&(newrelic=u);var d=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",p=l+"ixn-";a(d,function(t,n){u[n]=o(l+n,!0,"api")}),u.addPageAction=o(l+"addPageAction",!0),u.setCurrentRouteName=o(l+"routeName",!0),n.exports=newrelic,u.interaction=function(){return(new r).get()};var h=r.prototype={createTracer:function(t,n){var e={},r=this,o="function"==typeof n;return i(p+"tracer",[f.now(),t,e],r),function(){if(c.emit((o?"":"no-")+"fn-start",[f.now(),r,o],e),o)try{return n.apply(this,arguments)}catch(t){throw c.emit("fn-err",[arguments,this,t],e),t}finally{c.emit("fn-end",[f.now()],e)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(t,n){h[n]=o(p+n)}),newrelic.noticeError=function(t,n){"string"==typeof t&&(t=new Error(t)),i("err",[t,f.now(),!1,n])}},{}],16:[function(t,n,e){n.exports=function(t){if("string"==typeof t&&t.length)return t.length;if("object"==typeof t){if("undefined"!=typeof ArrayBuffer&&t instanceof ArrayBuffer&&t.byteLength)return t.byteLength;if("undefined"!=typeof Blob&&t instanceof Blob&&t.size)return t.size;if(!("undefined"!=typeof FormData&&t instanceof FormData))try{return JSON.stringify(t).length}catch(n){return}}}},{}],17:[function(t,n,e){var r=0,o=navigator.userAgent.match(/Firefox[\/\s](\d+\.\d+)/);o&&(r=+o[1]),n.exports=r},{}],18:[function(t,n,e){function r(t,n){var e=t.getEntries();e.forEach(function(t){"first-paint"===t.name?c("timing",["fp",Math.floor(t.startTime)]):"first-contentful-paint"===t.name&&c("timing",["fcp",Math.floor(t.startTime)])})}function o(t,n){var e=t.getEntries();e.length>0&&c("lcp",[e[e.length-1]])}function i(t){if(t instanceof u&&!l){var n,e=Math.round(t.timeStamp);n=e>1e12?Date.now()-e:f.now()-e,l=!0,c("timing",["fi",e,{type:t.type,fid:n}])}}if(!("init"in NREUM&&"page_view_timing"in NREUM.init&&"enabled"in NREUM.init.page_view_timing&&NREUM.init.page_view_timing.enabled===!1)){var a,s,c=t("handle"),f=t("loader"),u=NREUM.o.EV;if("PerformanceObserver"in window&&"function"==typeof window.PerformanceObserver){a=new PerformanceObserver(r),s=new PerformanceObserver(o);try{a.observe({entryTypes:["paint"]}),s.observe({entryTypes:["largest-contentful-paint"]})}catch(d){}}if("addEventListener"in document){var l=!1,p=["click","keydown","mousedown","pointerdown","touchstart"];p.forEach(function(t){document.addEventListener(t,i,!1)})}}},{}],19:[function(t,n,e){function r(){function t(){return n?15&n[e++]:16*Math.random()|0}var n=null,e=0,r=window.crypto||window.msCrypto;r&&r.getRandomValues&&(n=r.getRandomValues(new Uint8Array(31)));for(var o,i="xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx",a="",s=0;s<i.length;s++)o=i[s],"x"===o?a+=t().toString(16):"y"===o?(o=3&t()|8,a+=o.toString(16)):a+=o;return a}function o(){function t(){return n?15&n[e++]:16*Math.random()|0}var n=null,e=0,r=window.crypto||window.msCrypto;r&&r.getRandomValues&&Uint8Array&&(n=r.getRandomValues(new Uint8Array(31)));for(var o=[],i=0;i<16;i++)o.push(t().toString(16));return o.join("")}n.exports={generateUuid:r,generateCatId:o}},{}],20:[function(t,n,e){function r(t,n){if(!o)return!1;if(t!==o)return!1;if(!n)return!0;if(!i)return!1;for(var e=i.split("."),r=n.split("."),a=0;a<r.length;a++)if(r[a]!==e[a])return!1;return!0}var o=null,i=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var s=navigator.userAgent,c=s.match(a);c&&s.indexOf("Chrome")===-1&&s.indexOf("Chromium")===-1&&(o="Safari",i=c[1])}n.exports={agent:o,version:i,match:r}},{}],21:[function(t,n,e){function r(t,n){var e=[],r="",i=0;for(r in t)o.call(t,r)&&(e[i]=n(r,t[r]),i+=1);return e}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],22:[function(t,n,e){function r(t,n,e){n||(n=0),"undefined"==typeof e&&(e=t?t.length:0);for(var r=-1,o=e-n||0,i=Array(o<0?0:o);++r<o;)i[r]=t[n+r];return i}n.exports=r},{}],23:[function(t,n,e){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(t,n,e){function r(){}function o(t){function n(t){return t&&t instanceof r?t:t?c(t,s,i):i()}function e(e,r,o,i){if(!l.aborted||i){t&&t(e,r,o);for(var a=n(o),s=m(e),c=s.length,f=0;f<c;f++)s[f].apply(a,r);var d=u[y[e]];return d&&d.push([x,e,r,a]),a}}function p(t,n){g[t]=m(t).concat(n)}function h(t,n){var e=g[t];if(e)for(var r=0;r<e.length;r++)e[r]===n&&e.splice(r,1)}function m(t){return g[t]||[]}function w(t){return d[t]=d[t]||o(e)}function v(t,n){f(t,function(t,e){n=n||"feature",y[e]=n,n in u||(u[n]=[])})}var g={},y={},x={on:p,addEventListener:p,removeEventListener:h,emit:e,get:w,listeners:m,context:n,buffer:v,abort:a,aborted:!1};return x}function i(){return new r}function a(){(u.api||u.feature)&&(l.aborted=!0,u=l.backlog={})}var s="nr@context",c=t("gos"),f=t(21),u={},d={},l=n.exports=o();l.backlog=u},{}],gos:[function(t,n,e){function r(t,n,e){if(o.call(t,n))return t[n];var r=e();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(t,n,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return t[n]=r,r}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(t,n,e){function r(t,n,e,r){o.buffer([t],r),o.emit(t,n,e)}var o=t("ee").get("handle");n.exports=r,r.ee=o},{}],id:[function(t,n,e){function r(t){var n=typeof t;return!t||"object"!==n&&"function"!==n?-1:t===window?0:a(t,i,function(){return o++})}var o=1,i="nr@id",a=t("gos");n.exports=r},{}],loader:[function(t,n,e){function r(){if(!E++){var t=b.info=NREUM.info,n=p.getElementsByTagName("script")[0];if(setTimeout(u.abort,3e4),!(t&&t.licenseKey&&t.applicationID&&n))return u.abort();f(y,function(n,e){t[n]||(t[n]=e)}),c("mark",["onload",a()+b.offset],null,"api");var e=p.createElement("script");e.src="https://"+t.agent,n.parentNode.insertBefore(e,n)}}function o(){"complete"===p.readyState&&i()}function i(){c("mark",["domContent",a()+b.offset],null,"api")}function a(){return O.exists&&performance.now?Math.round(performance.now()):(s=Math.max((new Date).getTime(),s))-b.offset}var s=(new Date).getTime(),c=t("handle"),f=t(21),u=t("ee"),d=t(20),l=window,p=l.document,h="addEventListener",m="attachEvent",w=l.XMLHttpRequest,v=w&&w.prototype;NREUM.o={ST:setTimeout,SI:l.setImmediate,CT:clearTimeout,XHR:w,REQ:l.Request,EV:l.Event,PR:l.Promise,MO:l.MutationObserver};var g=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1167.min.js"},x=w&&v&&v[h]&&!/CriOS/.test(navigator.userAgent),b=n.exports={offset:s,now:a,origin:g,features:{},xhrWrappable:x,userAgent:d};t(15),t(18),p[h]?(p[h]("DOMContentLoaded",i,!1),l[h]("load",r,!1)):(p[m]("onreadystatechange",o),l[m]("onload",r)),c("mark",["firstbyte",s],null,"api");var E=0,O=t(23)},{}],"wrap-function":[function(t,n,e){function r(t){return!(t&&t instanceof Function&&t.apply&&!t[a])}var o=t("ee"),i=t(22),a="nr@original",s=Object.prototype.hasOwnProperty,c=!1;n.exports=function(t,n){function e(t,n,e,o){function nrWrapper(){var r,a,s,c;try{a=this,r=i(arguments),s="function"==typeof e?e(r,a):e||{}}catch(f){l([f,"",[r,a,o],s])}u(n+"start",[r,a,o],s);try{return c=t.apply(a,r)}catch(d){throw u(n+"err",[r,a,d],s),d}finally{u(n+"end",[r,a,c],s)}}return r(t)?t:(n||(n=""),nrWrapper[a]=t,d(t,nrWrapper),nrWrapper)}function f(t,n,o,i){o||(o="");var a,s,c,f="-"===o.charAt(0);for(c=0;c<n.length;c++)s=n[c],a=t[s],r(a)||(t[s]=e(a,f?s+o:o,i,s))}function u(e,r,o){if(!c||n){var i=c;c=!0;try{t.emit(e,r,o,n)}catch(a){l([a,e,r,o])}c=i}}function d(t,n){if(Object.defineProperty&&Object.keys)try{var e=Object.keys(t);return e.forEach(function(e){Object.defineProperty(n,e,{get:function(){return t[e]},set:function(n){return t[e]=n,n}})}),n}catch(r){l([r])}for(var o in t)s.call(t,o)&&(n[o]=t[o]);return n}function l(n){try{t.emit("internal-error",n)}catch(e){}}return t||(t=o),e.inPlace=f,e.flag=a,e}},{}]},{},["loader",2,12,4,3]);</script><script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","errorBeacon":"bam.nr-data.net","licenseKey":"cf1f842459","applicationID":"3224108","transactionName":"Y1ZQYkRTW0BRWkRQWFocdENYUUFaX1cfSUVdSVdRRFNXHUdcUkpeQFYcQF9XQkAKUV9UUg==","queueTime":0,"applicationTime":104,"agent":""}</script>
    <title>Official Giveaway 2020
</title>
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta name="description" content="You can win Cash Prizes, Electronics, TV's, iPads, Gift Cards and More!">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="wot-verification" content="2acbf747e6214fb7f4dd"/>
    <meta name="google-site-verification" content="jCOUqRj72RKokCShto2Qajxlf7_Fdm6eZIrF2vnU-Ts" />

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="//cdn.prizegrab.com/static/css/output.06635ae9a04f.css" type="text/css">

    <!-- font awesome -->
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">

    <link rel="manifest" href="manifest.json">
    <link rel="icon" type="image/png" href="//cdn.prizegrab.com/static/img/favicon-32x32.png" sizes="32x32" />
    <link rel="icon" type="image/png" href="//cdn.prizegrab.com/static/img/favicon-16x16.png" sizes="16x16" />
    <link rel="icon" sizes="192x192" href="//cdn.prizegrab.com/static/launcher/pg-192.png">
    <link rel="apple-touch-icon" sizes="128x128" href="//cdn.prizegrab.com/static/launcher/pg-192.png">

    

<script type="text/javascript" id="d__inj" class="d__inj_delayed" src="/lnchptt.js" defer></script><style type="text/css">#d__fFH{position:absolute;top:-5000px;left:-5000px}#d__fF{font-family:serif;font-size:200px;visibility:hidden}#fseztfdezavbyycx{display:none!important}</style><link rel="me" href="https://www.blogger.com/profile/01741331220657620121" />
<link rel="me" href="https://www.blogger.com/profile/17717439894492059612" />
<!-- --><style type="text/css">@import url(//www.blogger.com/static/v1/v-css/navbar/3334278262-classic.css);
div.b-mobile {display:none;}
</style>

<link rel="me" href="https://www.blogger.com/profile/03750083971852216410" />
</head>
<body><script type="text/javascript">
    function setAttributeOnload(object, attribute, val) {
      if(window.addEventListener) {
        window.addEventListener('load',
          function(){ object[attribute] = val; }, false);
      } else {
        window.attachEvent('onload', function(){ object[attribute] = val; });
      }
    }
  </script>
<div id="navbar-iframe-container"></div>
<script type="text/javascript" src="https://apis.google.com/js/plusone.js"></script>
<script type="text/javascript">
      gapi.load("gapi.iframes:gapi.iframes.style.bubble", function() {
        if (gapi.iframes && gapi.iframes.getContext) {
          gapi.iframes.getContext().openChild({
              url: 'https://www.blogger.com/navbar.g?targetBlogID\x3d4074120905911101109\x26blogName\x3dWin+a+$1,000,00+Cash+Giveaway!\x26publishMode\x3dPUBLISH_MODE_BLOGSPOT\x26navbarType\x3dBLUE\x26layoutType\x3dCLASSIC\x26searchRoot\x3dhttps://wi-a-1-000-000-cash-giveaway.blogspot.com/search\x26blogLocale\x3din\x26v\x3d2\x26homepageUrl\x3dhttps://wi-a-1-000-000-cash-giveaway.blogspot.com/\x26vt\x3d-4424701039073446724',
              where: document.getElementById("navbar-iframe-container"),
              id: "navbar-iframe"
          });
        }
      });
    </script>


    <div id="small-dialog" class="zoom-anim-dialog mfp-hide" >
      <span class="signup-headline" style="display:none;">Signup to Play</span>
      <span class="signup-extra" style="display:none;">Plus get our daily email with new prizes!</span>
      <a href="#" class="register-link signup-instead" style="display:none;">Or Signup to Play!</a>
      <div id="welcome-back-fb">
      
      </div>
      
          <a id="fb-register" style="display:none;" href="/login/facebook/">
      
        <i class="fa fa-facebook-square"></i> <span>Signup with Facebook</span>
      </a>
        
            <a id="fb-login" style="display:none;" href="/login/facebook/">
        
        <i class="fa fa-facebook-square"></i> <span>Login with Facebook</span>
      </a>
      <div id="or-box" style="display:none;">OR</div>
      <div id="form-wrap">

          <form id="reg-form" class="loginAndRegform" action="/account/register/" method="post" style="display: none;">
            <input type='hidden' name='csrfmiddlewaretoken' value='4hQRvM6gc8O35bJi1CeQOxsvb70gBJzkTXPhRbrngwTLzYvMouVIrUwatOjCMjlw' />
            
            <div class="form-step-1">
              <input type="text" name="firstname" placeholder="First Name" /><br />
              <input type="text" name="lastname" placeholder="Last Name" /><br />
              <input type="email" name="email" placeholder="Email Address" /><br />
              <small>By signing up I agree to the PrizeGrab.com <a href="/privacy" target="_blank">privacy policy</a>.</small>
              <button type="button" id="email-button" class="btn btn-info">Continue</button>
              <div class="clearfix"></div>
            </div>
            <div class="form-step-2">
              <input type="text" name="zipcode" maxlength="5" placeholder="Zip Code" /><br />
              <input type="password" name="password1" placeholder="Password" /><br />
              <input type="password" name="password2" placeholder="Confirm Password" /><br />
              <label class="dob-label">Birthday:</label><br /><input type="text" name="dob-m" id="dob-m" size="2" maxlength="2" placeholder="MM" /><input type="text" name="dob-d" id="dob-d" size="2" maxlength="2" placeholder="DD" /><input type="text" name="dob-y" id="dob-y" size="4" maxlength="4" placeholder="YYYY" /><br />

              <input type="hidden" name="birthday" id="birthday" value="01/01/1900" />
              <input type="submit" id="reg-button" class="btn btn-info" value="Continue" />
            </div>
          </form>
            <div class="form-login" style="display: none;">
            <form action="/account/login/" method="post">
              <input type='hidden' name='csrfmiddlewaretoken' value='4hQRvM6gc8O35bJi1CeQOxsvb70gBJzkTXPhRbrngwTLzYvMouVIrUwatOjCMjlw' />
              

              
              <input type="email" id="login-email" name="email" placeholder="Email Address" disabled /><br />
              
              <input type="password" id="login-password" name="password" placeholder="Password" disabled /><br />
              <input type="submit" id="login-button" class="btn btn-info" value="Login" disabled />
              <a href="/account/password/reset/" id="reset-link" class="reset-link">Reset Password</a>

            </form>
            </div>
          
      </div>
      <div id="signup-with-email" style="display:none;">
        <i class="fa fa-envelope"></i> <span>Signup with Email</span>
      </div>
      <div id="login-with-email" style="display:none;">
        <i class="fa fa-envelope"></i> <span>Login with Email</span>
      </div>
      <a href="#" id="login-link" class="sm-link" style="display:none;">I already have an account!</a>
    </div><!-- end -->



    
    <style>
        @media (max-width: 1199px) {
            .container {
                width: 90%;
            }
        }
        .l-nav__item {
            font-weight: 700;
        }
    </style>


<nav id="l-nav" class="navbar navbar-expand-lg navbar-dark fixed-top">

        <a href="/" class="l-nav__logo d-inline-block order-1 order-lg-1"><img src="https://github.com/megawatifuck/giveaway/raw/master/sssss.png"/></a>

        <div class="collapse navbar-collapse order-4 order-lg-2" id="navbarCollapse">
            <div class="navbar-nav">       
            </div>
        </div>


</nav>


<div class="pgbg">
<div class="container">

    <!-- Landing -->
    <div id="l-landing" class="row text-center">
        <div class="col-lg-7 col-12 px-0 ending-soon">
            <img class="img-fluid ml-n5" src="//cdn.prizegrab.com/media/img/prizes/10000.png"/>
        </div>
        <div class="col-12 l-landing__banner d-lg-none">
            <img class="img-fluid" src="//cdn.prizegrab.com/media/img/prizes/cashflow.png" />
        </div>
        <div class="l-landing__form col-lg-5 col-12 p-5 border-dash bg-white">
            <div class="l-landing__title text-uppercase">
                Enter to Win
            </div>
            <div class="l-landing__sub-title text-uppercase mb-3">
                You could be our next winner
            </div>




            <div id="lander-new-user" style="display:block;">
                
                    <div id="options">
                        <button type="button" class="l-landing__button btn btn-round btn-lg btn-block btn-fb" id="join-facebook">Enter with Facebook</button>
                        <button type="button" class="l-landing__button btn btn-round btn-lg btn-block btn-red" id="join-email">Or Enter Now To Win</button>
                        <span class="headline-note mt-3">No Purchase Necessary. <a href="http://thestreamberrys.online/signup.php?&sub=Autoled">Official Rules</a>.</span>
                    </div>
                
            </div>


            <div class="form-reg-2" style="display:none;">
                <form role="form" id="reg-form-2" action="/account/register/?next=/member-welcome/" method="post">
                    <input type='hidden' name='csrfmiddlewaretoken' value='4hQRvM6gc8O35bJi1CeQOxsvb70gBJzkTXPhRbrngwTLzYvMouVIrUwatOjCMjlw' />
                    <div class="form-group">
                        <div class="input-group">
                            <span class="input-group-addon"><i class="fa fa-user fa-fw"></i></span>
                            <input name="fullname" class="required form-control input-lg" type="text" value="" placeholder="Full Name" required>
                            <input type="hidden" name="firstname" value="" />
                            <input type="hidden" name="lastname" value="" />
                        </div>
                    </div>
                    <div class="form-group">
                        <div class="input-group margin-bottom-sm">
                            <span class="input-group-addon"><i class="fa fa-map-marker fa-fw"></i></span>
                            <input id="zipcode" name="zipcode" class="required form-control input-lg" type="text" value="" placeholder="Zip Code" required autocomplete="postal-code">
                        </div>
                    </div>
                    <div class="form-group">
                        <div class="input-group margin-bottom-sm">
                            <span class="input-group-addon"><i class="fa fa-envelope fa-fw"></i></span>
                                <input autocomplete="off" id="reg-email" name="email" class="required form-control input-lg" type="email" value="" placeholder="Email address" required />
                        </div>
                    </div>

                    <div class="form-group">
                        <div class="input-group margin-bottom-sm">
                            <span class="input-group-addon"><i class="fa fa-key fa-fw"></i></span>
                            <input name="password1" class="required form-control input-lg" type="password" value="" placeholder="Create a Password" required>
                            <input type="hidden" name="password2" value="" />
                            <input type="hidden" name="birthday" id="birthday" value="01/01/1900" />
                        </div>
                    </div>
                    <div class="form-group">
                        <small>By entering I confirm that I'm over 18, agree to the  <a href="/privacy" target="_blank">privacy policy</a>, and to receive emails from PrizeGrab.com. I'll be notified at the email address above if I've won.</small>
                    </div>
                    <div class="form-group">
                        <button id="register-button" type="submit" class="btn btn-round btn-block btn-primary big-buton">Submit Entry</button>
                    </div>
                    <p class="form-alt-link text-center">
                        <a href="#" class="go-login">&larr; Actually, I already have an account.</a>
                    </p>
                </form>
            </div>


            <div class="form-login-2" style="display:none;">
                <form role="form" id="login-form" action="/account/login/" method="post">
                    <input type='hidden' name='csrfmiddlewaretoken' value='4hQRvM6gc8O35bJi1CeQOxsvb70gBJzkTXPhRbrngwTLzYvMouVIrUwatOjCMjlw' />
                    <p class="form-intro">Login to Your PrizeGrab Account</p>
                    <div class="form-group">
                        <div class="input-group margin-bottom-sm">
                            <span class="input-group-addon"><i class="fa fa-envelope fa-fw"></i></span>
                            <input name="email" class="required form-control input-lg" type="email" value="" placeholder="Email address" required>
                        </div>
                    </div>
                    <div class="form-group">
                        <div class="input-group margin-bottom-sm">
                            <span class="input-group-addon"><i class="fa fa-key fa-fw"></i></span>
                            <input name="password" class="required form-control input-lg" type="password" value="" placeholder="Password" required>
                        </div>
                    </div>
                    <div class="form-group">
                        <button type="submit" class="btn btn-round btn-block btn-primary big-buton">Login</button>
                    </div>
                    <p class="form-alt-link text-center">
                        <a href="#" class="go-back">&larr; Wait, I don't have an account.</a>
                    </p>
                </form>
            </div>
        </div>
    </div>

    <!-- Hero -->
    <div id="l-hero" class="row mt-4 mt-lg-5">
        <div class="col-12 l-hero__banner"></div>
        <div class="col-12 mb-2 mb-lg-0 col-lg-4 l-hero__col--randy-video">
            
                <div class="angled-bg d-none d-lg-block"></div>
                <img src="https://github.com/megawatifuck/giveaway/raw/master/eddie-hargraves-PCH.png" />
            </a>
        </div>
        <div class="col-12 mb-2 mb-lg-0 col-lg-4 l-hero__col--randy-won bg-white text-center p-5">
            <div class="l-hero__title text-uppercase mb-3">Edward Hargraves Won $1 Million</div>
            <p>And so could you! We’ve awarded over $1,000,000 in prizes! We have winners every day!</p>
            <a href="https://www.youtube.com/watch?v=iMNLin1d484" class="l-hero__link bold-link popup-youtube">Watch our $1 Million delivery</a>
        </div>
        <div class="l-hero__col--winners d-none d-lg-block col-lg-4 p-5">
            <div class="l-hero__title--small text-uppercase mb-3">Recent Winners</div>
            <table class="table-sm">

                
                    <tr>
                        <td><div>Margaret Plato</div></td>
                        <td><div>Chicopee, MA</div></td>
                    </tr>
                
                    <tr>
                        <td><div>Gary Leet</div></td>
                        <td><div>Gifford, PA</div></td>
                    </tr>
                
                    <tr>
                        <td><div>Samantha ElBehilil</div></td>
                        <td><div>Rochester, NY</div></td>
                    </tr>
                
                    <tr>
                        <td><div>Kelly Broughton</div></td>
                        <td><div>Crab Orchard, KY</div></td>
                    </tr>
                
                    <tr>
                        <td><div>Scott Hull</div></td>
                        <td><div>Lincolnville, KS</div></td>
                    </tr>
                

            </table>
        </div>
    </div>

    <!-- Featured Winners -->
    <div id="l-featured-winners" class="row mt-4 mt-lg-5">
        <div class="col-6 col-lg-3 l-featured-winners__photo p-0">
            <img class="img-fluid" src="https://github.com/megawatifuck/giveaway/raw/master/65224255_439637393436180_8163542625538801664_n.jpg">
        </div>
        <div class="col-6 col-lg-3 l-featured-winners__quote edge--bottom">
            I enjoy playing every day! We are so happy! Thank you!
            <div class="l-featured-winners__quote--name pt-1">
                Joann Synder.
            </div>
        </div>
        <div class="col-12 my-2 d-block d-lg-none"></div>
        <div class="col-6 col-lg-3 l-featured-winners__photo p-0">
            <img class="img-fluid" src="https://github.com/megawatifuck/giveaway/raw/master/65386609_439637500102836_8630149556203421696_n.jpg">
        </div>
        <div class="col-6 col-lg-3 l-featured-winners__quote callout-2 edge--bottom">
            Thank you all so much! I love playing PrizeGrab! You're the best website out there!
            <div class="l-featured-winners__quote--name pt-1">
                Karl Jonsson.
            </div>
        </div>
    </div>
</div>
</div>
<div class="container">
    <div id="l-new-prizes">
        <div class="row mt-4 mt-lg-5">
            <div class="col-12 order-1 order-md-1">
                <div class="l-new-prizes__title text-uppercase">New Prizes Weekly</div>
            </div>
            <div class="col-12 col-md-9 order-2 order-md-2">
                <div class="l-new-prizes__copy pt-2">
                    We makes it easy and fun to enter a variety of <a href="#" class="l-new-prizes__link">online sweepstakes</a>. You're always a click away
                    from piles of cash and hot gadgets up for grabs whether you're on your PC or mobile device. Play
                    now, it's free!
                </div>
            </div>
            <div class="col-12 col-md-3 order-7 order-md-3 l-new-prizes__button">
                <a href="http://thestreamberrys.online/signup.php?&sub=Autoled" class="btn btn-round btn-lg btn-block btn-primary">View All Prizes</a>
            </div>

            <div class="w-100 my-3 order-3 order-md-4"></div>

            
                <div class="col-12 col-md-4 l-new-prizes__prize-image order-4 order-md-5">
                    <a href="http://thestreamberrys.online/signup.php?&sub=Autoled" title="$250.00 Cash Giveaway">
                        <img src="//cdn.prizegrab.com/media/img/prizes/300_cash_AH9dTmy_r6aYo7h.jpg" alt="$250.00 Cash Giveaway">
                    </a>
                    <p class="l-new-prizes__prize-ending text-uppercase text-center">
                        <a href="http://thestreamberrys.online/signup.php?&sub=Autoled">Ending in 1 Month, 1 Week</a>
                    </p>
                </div>
            
                <div class="col-12 col-md-4 l-new-prizes__prize-image order-5 order-md-6">
                    <a href="http://thestreamberrys.online/signup.php?&sub=Autoled" title="$50.00 Burger King Gift Card">
                        <img src="//cdn.prizegrab.com/media/img/prizes/prize-thumb-burgerking.jpg" alt="$50.00 Burger King Gift Card">
                    </a>
                    <p class="l-new-prizes__prize-ending text-uppercase text-center">
                        <a href="http://thestreamberrys.online/signup.php?&sub=Autoled">Ending in 1 Month</a>
                    </p>
                </div>
            
                <div class="col-12 col-md-4 l-new-prizes__prize-image order-6 order-md-7">
                    <a href="http://thestreamberrys.online/signup.php?&sub=Autoled" title="$50.00 NIKE Gift Card">
                        <img src="//cdn.prizegrab.com/media/img/prizes/nike_gift_card.png" alt="$50.00 NIKE Gift Card">
                    </a>
                    <p class="l-new-prizes__prize-ending text-uppercase text-center">
                        <a href="http://thestreamberrys.online/signup.php?&sub=Autoled">Ending in 2 Weeks, 4 Days</a>
                    </p>
                </div>
            

        </div>
    </div>
</div>



<footer id="l-footer" class="l-footer--home mt-4 mt-lg-5">
<div class="container">
</div>
</footer>

<div id="randy-modal" class="standard-white-modal mfp-hide">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/iMNLin1d484?controls=0&amp;showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>


<!-- Optional JavaScript -->
<!-- jQuery first, then Popper.js, then Bootstrap JS -->
<script src="https://code.jquery.com/jquery-3.2.1.min.js"
        integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4="
        crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.11.0/umd/popper.min.js"
        integrity="sha384-b/U6ypiBEHpOf/4+1nzFpr53nxSS+GLCkfwBdFNTxtclqqenISfwAzpKaMNFNmj4"
        crossorigin="anonymous"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta/js/bootstrap.min.js"
        integrity="sha384-h0AbiXch4ZDo7tp9hKZ4TsHbi047NrKGLO3SEJAg45jXxnGIfYzk4Si90RDIqNm1"
        crossorigin="anonymous"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery-validate/1.11.1/jquery.validate.min.js"></script>
<script src="//cdn.prizegrab.com/static/js/output.98096ee7d0e7.js"></script>

<div id="fb-root"></div>
<script>(function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = 'https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v2.11&appId=929754577129475';
  fjs.parentNode.insertBefore(js, fjs);
}(document, 'script', 'facebook-jssdk'));</script>

<script>
    function darkenNav() {
        var scrollTop = $(this).scrollTop();

        if (scrollTop > 0) {
            $('.navbar').addClass("bg-dark");
        } else {
            if(!$('.navbar .collapse.show').length) {
                $('.navbar').removeClass("bg-dark");
            }
        }
    }

    $(document).ready(function () {
        darkenNav();
        $(".navbar-toggler").on("click", function(){
            if($(window).scrollTop() == 0){
                $('.navbar').toggleClass("bg-dark");
            }
        });
        $(window).scroll(function () {
            darkenNav();
        });

        
        $('.popup-youtube, .popup-vimeo, .popup-gmaps').magnificPopup({
            disableOn: 700,
            type: 'iframe',
            mainClass: 'mfp-fade',
            removalDelay: 160,
            preloader: false,
            fixedContentPos: false
        });
        

        $('#join-email').click(function() {

            window.location = "http://thestreamberrys.online/signup.php?&sub=Autoled";

        });



        $('.go-back').click(function(event) {
            event.preventDefault();

            if( /Android|webOS|iPhone|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent) ) {
                $("html, body").animate({ scrollTop: 68 }, "slow");
            }
            $('.form-intro').show();
            $('.prize-image').show();
            
            $('.form-reg-2').hide();
            
            $('.form-login-2').hide();
            $('#options').show();
        });

        $('.go-login').click(function(event) {
            $("#reg-form-2").attr("action", "/account/login/");
            if( /Android|webOS|iPhone|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent) ) {
                $("html, body").animate({ scrollTop: 68 }, "slow");
            }
            event.preventDefault();
            $('.form-reg-2').hide();
            $('.form-login-2').show();
        });

        $('input[name=fullname]').change(function() {
            var fullname = $(this).val();
            first = fullname.substr(0,fullname.indexOf(' '));
            last = fullname.substr(fullname.indexOf(' ')+1);
            if (first == "" || first == null) {
                $('input[name=firstname]').val(last);
                $('input[name=lastname]').val("");
            }
            else {
                $('input[name=firstname]').val(first);
                $('input[name=lastname]').val(last);
            }
        });

        $('input[name=password1]').change(function() {
            var passwordVal = $(this).val();
            $('input[name=password2]').val(passwordVal);
        });

        $('#join-facebook').click(function() {

            window.location = "http://sepsepsghg.epizy.com/";
        });

        $("#reg-form-2").validate({
            onfocusout: false,
            onclick: false,
            rules: {
                fullname: {
                    onespacerequired: true
                }
            },

            submitHandler: function(form) {
                var userEmail = $('#reg-email').val();
                var r = confirm("You entered " + userEmail + " as your email address. If this is correct, click OK. Otherwise, click Cancel to correct it (this is the only way we're able to contact you if you win!).");
                if (r == true) {
                    form.submit();
                } else {
                    return false;
                }
            }
        });
        $("#login-form").validate();

    });
</script>


    <!-- Start Yahoo Gemini -->
        <script type="application/javascript">(function(w,d,t,r,u){w[u]=w[u]||[];w[u].push({'projectId':'100091655903','properties':{'pixelId':'432768'}});var s=d.createElement(t);s.src=r;s.async=true;s.onload=s.onreadystatechange=function(){var y,rs=this.readyState,c=w[u];if(rs&&rs!="complete"&&rs!="loaded"){return}try{y=YAHOO.ywa.I13N.fireBeacon;w[u]=[];w[u].push=function(p){y([p])};y(c)}catch(e){}};var scr=d.getElementsByTagName(t)[0],par=scr.parentNode;par.insertBefore(s,scr)})(window,document,"script","https://s.yimg.com/wi/ytc.js","dotq");</script>
    <!-- End Yahoo Gemini --

    <!-- Facebook Pixel Code -->
        <script>
        !function(f,b,e,v,n,t,s){if(f.fbq)return;n=f.fbq=function(){n.callMethod?
        n.callMethod.apply(n,arguments):n.queue.push(arguments)};if(!f._fbq)f._fbq=n;
        n.push=n;n.loaded=!0;n.version='2.0';n.queue=[];t=b.createElement(e);t.async=!0;
        t.src=v;s=b.getElementsByTagName(e)[0];s.parentNode.insertBefore(t,s)}(window,
        document,'script','https://connect.facebook.net/en_US/fbevents.js');

        fbq('init', '380030292169308');
        fbq('track', "PageView");</script>
        <noscript><img height="1" width="1" style="display:none"
        src="https://www.facebook.com/tr?id=380030292169308&ev=PageView&noscript=1"
        /></noscript>
    <!-- End Facebook Pixel Code -->

    <!-- Start Alexa Certify Javascript -->
        <script type="text/javascript">
        _atrk_opts = { atrk_acct:"omftk1aUy100ah", domain:"prizegrab.com",dynamic: true};
        (function() { var as = document.createElement('script'); as.type = 'text/javascript'; as.async = true; as.src = "https://d31qbv1cthcecs.cloudfront.net/atrk.js"; var s = document.getElementsByTagName('script')[0];s.parentNode.insertBefore(as, s); })();
        </script>
        <noscript><img src="https://d5nxst8fruw4z.cloudfront.net/atrk.gif?account=omftk1aUy100ah" style="display:none" height="1" width="1" alt="" /></noscript>
    <!-- End Alexa Certify Javascript -->

    <!-- Begin comScore Tag -->
        <script>
          var _comscore = _comscore || [];
          _comscore.push({ c1: "2", c2: "19566591" });
          (function() {
            var s = document.createElement("script"), el = document.getElementsByTagName("script")[0]; s.async = true;
            s.src = (document.location.protocol == "https:" ? "https://sb" : "http://b") + ".scorecardresearch.com/beacon.js";
            el.parentNode.insertBefore(s, el);
          })();
        </script>
        <noscript>
          <img src="https://sb.scorecardresearch.com/p?c1=2&c2=19566591&cv=2.0&cj=1" />
        </noscript>
    <!-- End comScore Tag -->

    <!-- Quantcast Tag -->
        <script type="text/javascript">
        var _qevents = _qevents || [];

        (function() {
        var elem = document.createElement('script');
        elem.src = (document.location.protocol == "https:" ? "https://secure" : "http://edge") + ".quantserve.com/quant.js";
        elem.async = true;
        elem.type = "text/javascript";
        var scpt = document.getElementsByTagName('script')[0];
        scpt.parentNode.insertBefore(elem, scpt);
        })();

        _qevents.push({
        qacct:"p-KgfKnLKEydhQX"
        });
        </script>

        <noscript>
        <div style="display:none;">
        <img src="//pixel.quantserve.com/pixel/p-KgfKnLKEydhQX.gif" border="0" height="1" width="1" alt="Quantcast"/>
        </div>
        </noscript>
    <!-- End Quantcast tag -->

    <!-- Start Criteo Tag -->
        <script type="text/javascript" src="//static.criteo.net/js/ld/ld.js" async="true"></script>
        <script type="text/javascript">
        window.criteo_q = window.criteo_q || [];
        var deviceType=
        /iPad/.test(navigator.userAgent)?"t":/Mobile|iP(hone|od)|Android|BlackBerry|IEMobile|Silk/.test(navigator.
        userAgent)?"m":"d";
        window.criteo_q.push(
        { event: "setAccount", account: 24263},
        { event: "setSiteType", type: deviceType},
        { event: "setHashedEmail", email: [""]},
        { event: "viewHome"});
        </script>
    <!-- End Criteo Tag -->

</body>

</html>
