﻿<script src="//cdnjs.cloudflare.com/ajax/libs/angular.js/1.2.20/angular.js"></script>
<script src="/js/contributors.js"></script>
<script src="/js/app.js"></script>
<link rel="stylesheet" href="/css/contributors.css" type="text/css" />

<div ng-app="ContributorsApp" ng-controller="ContributorsCtrl">
    <ul>
        <li ng-repeat="contributor in totalContributors" class="contributor">
            <a class="contributor-left" href="{{ contributor.html_url }}" target="_blank">
                <img ng-src="{{ contributor.avatar_url }}" alt="{{ contributor.login }}" class="contributor-image" />
            </a>
            <div class="contributor-body">
                <h4 class="contributor-heading">{{ contributor.login }}</h4>
                <p><a href="{{ contributor.html_url }}" target="_blank">{{ contributor.html_url }}</a></p>
                <p>Total Contributions: {{ contributor.contributions }}</p>
            </div>
        </li>
    </ul>
</div>