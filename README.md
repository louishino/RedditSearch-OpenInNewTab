# RedditSearch-OpenInNewTab
reddit上面的设置新标签页打开仅对首页有效 本脚本会让搜索到的帖子也在新标签页代开 
The setting on reddit to open a new tab page is only valid for the home page. This script will also open the searched posts in a new tab page.
新标签页打开是个好习惯 反复前进后退确实不浪费内存 只会浪费你的人生     
Opening in new tab is a good habit. Repeatedly going back and forth does not actually waste memory; it only wastes your life.

// ==UserScript==
// @name         Reddit 搜索结果新标签页打开帖子
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  在 Reddit 搜索结果中点击帖子链接时自动在新标签页中打开
// @author       You
// @match        https://www.reddit.com/search/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // 获取所有帖子标题链接
    const postLinks = document.querySelectorAll('a[data-testid="post-title"]');

    // 遍历每个链接并添加 target="_blank"
    postLinks.forEach(link => {
        link.setAttribute('target', '_blank');
    });

})();
