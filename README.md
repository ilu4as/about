async function streamLoop() {
    while(true) {
        // شغل البث
        document.querySelector('button[aria-label="Share Your Screen"]').click();
        await new Promise(r => setTimeout(r, 500));
        document.querySelectorAll('[class*="source"]')[0].click();
        await new Promise(r => setTimeout(r, 500));
        
        // وقف البث
        let stop = document.querySelector('button[aria-label="Stop Streaming"]');
        if(stop) stop.click();
        
        await new Promise(r => setTimeout(r, 500));
    }
}

streamLoop();
