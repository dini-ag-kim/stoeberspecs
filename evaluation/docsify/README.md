# docsify Demo

[docsify](https://docsify.js.org/) configuration for this demo:

    window.$docsify = {
        repo: "dini-ag-kim/oer-stoeberspecs",
        maxLevel: 3,
        loadSidebar: "sidebar.md",
        subMaxLevel: 3,
        auto2top: true,
        basePath: "https://dini-ag-kim.github.io/oer-stoeberspecs/evaluation/docsify/",
        relativePath: true,
        name: "docsify Demo",
        noEmoji: true,
        search: {
            maxAge: 86400000,
            paths: "auto",
            placeholder: "Suche",
            noData: "keine Treffer",
            depth: 2,
            hideOtherSidebarContent: false
        },
        pagination: {
            previousText: "zurück",
            nextText: "weiter",
            crossChapter: true
        }
    };
