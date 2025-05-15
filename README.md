# test-curseforge
ads remove


desktop.js
original
```
{let{isSubscribed:t,isShowingFtue:n,sideImage:o,showSubscribeText:r=!0}=e,[a,i]=(0,aW.useState)(!1),{gotoSubscriptionPage:s}=u9(),{defaultAdsLayout:l}=I8(),{t:c}=sg();return ud(uu.Ads.HighImpactAdLoaded,()=>{i(!0)}),ud(uu.Ads.HighImpactAdRemoved,()=>{i(!1)}),(0,k.jsx)(k.Fragment,{children:(0,k.jsxs)("aside",{className:(()=>{let e={"curseforge-ad":!0,subscribed:!1,[ex]:!1};return n||(e.subscribed=t,e[ex]=!1),cU.ClassNames(e)})(),children:[(0,k.jsx)(Ti,{background:o??Ts}),(0,k.jsx)("div",{className:"ad-inner",children:(0,k.jsx)(To,{show:!n&&!t,defaultAdsLayout:l,showHighImpactAd:a})}),(0,k.jsx)(cz,{when:!t&&!a&&r,children:(0,k.jsxs)("div",{className:"link-container",children:[(0,k.jsxs)("span",{children:[c(Tl.adsIntro),"."]})," ",(0,k.jsx)(cX,{isInline:!0,direction:cH.Top,text:${c(Tl.removeTooltip)},children:(0,k.jsx)("a",{className:"subscribe-link",onClick:()=>{s()},children:c(Tl.removeTitle)})})]})})]})})};
```

change to 
```
{let{isSubscribed:t,isShowingFtue:n,sideImage:o,showSubscribeText:r=!0}=e,[a,i]=(0,aW.useState)(!1),{gotoSubscriptionPage:s}=u9(),{defaultAdsLayout:l}=I8(),{t:c}=sg();return ud(uu.Ads.HighImpactAdLoaded,()=>{i(!0)}),ud(uu.Ads.HighImpactAdRemoved,()=>{i(!1)}),(0,k.jsx)(k.Fragment,{children:(0,k.jsxs)("aside",{className:(()=>{let e={"curseforge-ad":!0,subscribed:!0,[ex]:!1};return cU.ClassNames(e)})(),children:[(0,k.jsx)(Ti,{background:o??Ts}),(0,k.jsx)("div",{className:"ad-inner",children:(0,k.jsx)(To,{show:!n&&!t,defaultAdsLayout:l,showHighImpactAd:a})}),(0,k.jsx)(cz,{when:!t&&!a&&r,children:(0,k.jsxs)("div",{className:"link-container",children:[(0,k.jsxs)("span",{children:[c(Tl.adsIntro),"."]})," ",(0,k.jsx)(cX,{isInline:!0,direction:cH.Top,text:`${c(Tl.removeTooltip)}`,children:(0,k.jsx)("a",{className:"subscribe-link",onClick:()=>{s()},children:c(Tl.removeTitle)})})]})})]})})};
```

open dev tools
```
async initBrowserWindow(e,t){let r=true;this.window=new xc.BrowserWindow({icon:this.windowIconResolver.resolve(),width:e.width,height:e.height,minHeight:t.minHeight,minWidth:t.minWidth,x:e.x,y:e.y,show:!1,frame:!0,backgroundColor:"black",titleBarStyle:this.platformDetector.isMacOS()?"hidden":"default",trafficLightPosition:Eg,webPreferences:{devTools:r,preload:xm().join(xc.app.getAppPath(),"dist/preload/preload.js"),contextIsolation:!1,nodeIntegration:!1,additionalArguments:[`disableSentry=${!this.configuration.tracking.enable}`]}}),this.window.webContents.openDevTools()}
```

frame show
```
frame: !0,
```

set premium
```
{let e=AK(e=>e.subscription?.active);return S_(null),(0,k.jsxs)("div",{"data-testid":"subscription-page",className:"content-section scrollable",children:[e?(0,k.jsx)(Fi,{}):(0,k.jsx)(S7,{}),(0,k.jsx)(FA,{})]})}
```

change to
```
{let e=AK(()=>!0);return S_(null),(0,k.jsxs)("div",{"data-testid":"subscription-page",className:"content-section scrollable",children:[e?(0,k.jsx)(Fi,{}):(0,k.jsx)(S7,{}),(0,k.jsx)(FA,{})]})}
```
