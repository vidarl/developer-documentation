# REST API reference

## Root resources

### List Root Resources

List the Root Resources of the eZ Platform installation.

| Parameter   | Value       | 
| ----------- | ----------- | 
| URI         | `/`         | 
| Method      | GET         | 

#### Headers

##### Accept

If set the list is return in XML or JSON format

| Parameter                                                                 | Value                                                                     | 
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | 
| Type                                                                      | string                                                                    | 
| Default                                                                   | n/a                                                                       | 
| Required                                                                  | no                                                                        | 
| Example                                                                   | `application/vnd.ez.api.Root+xml`<br>`application/vnd.ez.api.Root+json`   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Root+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Root        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Root media-type="application/vnd.ez.api.Root+xml">
    <content media-type="" href="/api/ezp/v2/content/objects"/>
    <contentByRemoteId media-type="" href="/api/ezp/v2/content/objects{?remoteId}"/>
    <contentTypes media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/types"/>
    <contentTypeByIdentifier media-type="" href="/api/ezp/v2/content/types{?identifier}"/>
    <contentTypeGroups media-type="application/vnd.ez.api.ContentTypeGroupList+xml" href="/api/ezp/v2/content/typegroups"/>
    <contentTypeGroupByIdentifier media-type="" href="/api/ezp/v2/content/typegroups{?identifier}"/>
    <users media-type="application/vnd.ez.api.UserRefList+xml" href="/api/ezp/v2/user/users"/>
    <roles media-type="application/vnd.ez.api.RoleList+xml" href="/api/ezp/v2/user/roles"/>
    <rootLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2"/>
    <rootUserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5"/>
    <rootMediaFolder media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/43"/>
    <locationByRemoteId media-type="" href="/api/ezp/v2/content/locations{?remoteId}"/>
    <locationByPath media-type="" href="/api/ezp/v2/content/locations{?locationPath}"/>
    <trash media-type="application/vnd.ez.api.Trash+xml" href="/api/ezp/v2/content/trash"/>
    <sections media-type="application/vnd.ez.api.SectionList+xml" href="/api/ezp/v2/content/sections"/>
    <views media-type="application/vnd.ez.api.RefList+xml" href="/api/ezp/v2/views"/>
    <objectStateGroups media-type="application/vnd.ez.api.ObjectStateGroupList+xml" href="/api/ezp/v2/content/objectstategroups"/>
    <objectStates media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/{objectStateGroupId}/objectstates"/>
    <globalUrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/urlaliases"/>
    <urlWildcards media-type="application/vnd.ez.api.UrlWildcardList+xml" href="/api/ezp/v2/content/urlwildcards"/>
    <createSession media-type="application/vnd.ez.api.UserSession+xml" href="/api/ezp/v2/user/sessions"/>
    <refreshSession media-type="application/vnd.ez.api.UserSession+xml" href="/api/ezp/v2/user/sessions/{sessionId}/refresh"/>
</Root>
```

##### application/vnd.ez.api.Root+json

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Root        | 

```json
{
    "Root": {
        "_media-type": "application/vnd.ez.api.Root+json",
        "content": {
            "_href": "/api/ezp/v2/content/objects",
            "_media-type": ""
        },
        "contentByRemoteId": {
            "_href": "/api/ezp/v2/content/objects{?remoteId}",
            "_media-type": ""
        },
        "contentTypeByIdentifier": {
            "_href": "/api/ezp/v2/content/types{?identifier}",
            "_media-type": ""
        },
        "contentTypeGroupByIdentifier": {
            "_href": "/api/ezp/v2/content/typegroups{?identifier}",
            "_media-type": ""
        },
        "contentTypeGroups": {
            "_href": "/api/ezp/v2/content/typegroups",
            "_media-type": "application/vnd.ez.api.ContentTypeGroupList+json"
        },
        "contentTypes": {
            "_href": "/api/ezp/v2/content/types",
            "_media-type": "application/vnd.ez.api.ContentTypeInfoList+json"
        },
        "createSession": {
            "_href": "/api/ezp/v2/user/sessions",
            "_media-type": "application/vnd.ez.api.UserSession+json"
        },
        "globalUrlAliases": {
            "_href": "/api/ezp/v2/content/urlaliases",
            "_media-type": "application/vnd.ez.api.UrlAliasRefList+json"
        },
        "locationByPath": {
            "_href": "/api/ezp/v2/content/locations{?locationPath}",
            "_media-type": ""
        },
        "locationByRemoteId": {
            "_href": "/api/ezp/v2/content/locations{?remoteId}",
            "_media-type": ""
        },
        "objectStateGroups": {
            "_href": "/api/ezp/v2/content/objectstategroups",
            "_media-type": "application/vnd.ez.api.ObjectStateGroupList+json"
        },
        "objectStates": {
            "_href": "/api/ezp/v2/content/objectstategroups/{objectStateGroupId}/objectstates",
            "_media-type": "application/vnd.ez.api.ObjectStateList+json"
        },
        "roles": {
            "_href": "/api/ezp/v2/user/roles",
            "_media-type": "application/vnd.ez.api.RoleList+json"
        },
        "rootLocation": {
            "_href": "/api/ezp/v2/content/locations/1/2",
            "_media-type": "application/vnd.ez.api.Location+json"
        },
        "rootMediaFolder": {
            "_href": "/api/ezp/v2/content/locations/1/43",
            "_media-type": "application/vnd.ez.api.Location+json"
        },
        "rootUserGroup": {
            "_href": "/api/ezp/v2/user/groups/1/5",
            "_media-type": "application/vnd.ez.api.UserGroup+json"
        },
        "sections": {
            "_href": "/api/ezp/v2/content/sections",
            "_media-type": "application/vnd.ez.api.SectionList+json"
        },
        "trash": {
            "_href": "/api/ezp/v2/content/trash",
            "_media-type": "application/vnd.ez.api.Trash+json"
        },
        "urlWildcards": {
            "_href": "/api/ezp/v2/content/urlwildcards",
            "_media-type": "application/vnd.ez.api.UrlWildcardList+json"
        },
        "users": {
            "_href": "/api/ezp/v2/user/users",
            "_media-type": "application/vnd.ez.api.UserRefList+json"
        },
        "views": {
            "_href": "/api/ezp/v2/views",
            "_media-type": "application/vnd.ez.api.RefList+json"
        },
        "refreshSession": {
            "_media-type": "application\/vnd.ez.api.UserSession+json",
            "_href": "\/api\/ezp\/v2\/user\/sessions\/{sessionId}\/refresh"
        }
    }
}
```

## Managing bookmarks

### List bookmarks

Lists bookmarked locations for the current user

| Parameter     | Value         | 
| ------------- | ------------- | 
| URI           | `/bookmark`   | 
| Method        | GET           | 

#### Headers

##### Accept

If set the list is returned in XML or JSON format

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.BookmarkList+xml`<br>`application/vnd.ez.api.BookmarkList+json`   | 

#### Query Parameters

| Name                               | Type                               | Default                            | Required                           | Example                            | Description                        | 
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | 
| offset                             | integer                            | n/a                                | no                                 | n/a                                | The offset of the result set       | 
| limit                              | integer                            | 25                                 | no                                 | n/a                                | The number of bookmarks returned   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.BookmarkList+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | BookmarkList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<BookmarkList media-type="application/vnd.ez.api.BookmarkList+xml">
    <count>3</count>
    <Bookmark media-type="application/vnd.ez.api.Bookmark+xml" _href="/api/ezp/v2/bookmark/62">
        <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/62">
            <id>62</id>
            <priority>0</priority>
            <hidden>false</hidden>
            <invisible>false</invisible>
            <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2"/>
            <pathString>/1/2/62/</pathString>
            <depth>2</depth>
            <childCount>0</childCount>
            <remoteId>5f1bb9f8ea33374082372d6970eccc4b</remoteId>
            <Children media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/2/62/children"/>
            <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/61"/>
            <sortField>NAME</sortField>
            <sortOrder>ASC</sortOrder>
            <UrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/locations/1/2/62/urlaliases"/>
            <ContentInfo media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61">
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61" remoteId="2c90ebb85a849a377a8df1ba775dbba4" id="61">
                    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
                    <Name>777</Name>
                    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/61/versions"/>
                    <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/currentversion"/>
                    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
                    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/61/locations"/>
                    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                    <lastModificationDate>2018-11-09T14:50:16+01:00</lastModificationDate>
                    <publishedDate>2018-11-09T14:50:16+01:00</publishedDate>
                    <mainLanguageCode>eng-GB</mainLanguageCode>
                    <currentVersionNo>1</currentVersionNo>
                    <alwaysAvailable>false</alwaysAvailable>
                    <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/61/objectstates"/>
                </Content>
            </ContentInfo>
        </Location>
    </Bookmark>
    <Bookmark media-type="application/vnd.ez.api.Bookmark+xml" _href="/api/ezp/v2/bookmark/60">
        <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/60">
            <id>60</id>
            <priority>0</priority>
            <hidden>false</hidden>
            <invisible>false</invisible>
            <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2"/>
            <pathString>/1/2/60/</pathString>
            <depth>2</depth>
            <childCount>0</childCount>
            <remoteId>bcbb52b6384679f75c80123868ce9374</remoteId>
            <Children media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/2/60/children"/>
            <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/59"/>
            <sortField>NAME</sortField>
            <sortOrder>ASC</sortOrder>
            <UrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/locations/1/2/60/urlaliases"/>
            <ContentInfo media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/59">
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/59" remoteId="4b63356b7fe92db9c39f64c37baa53d3" id="59">
                    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
                    <Name>555</Name>
                    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/59/versions"/>
                    <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/59/currentversion"/>
                    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
                    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/59/locations"/>
                    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                    <lastModificationDate>2018-11-09T14:48:58+01:00</lastModificationDate>
                    <publishedDate>2018-11-09T14:48:58+01:00</publishedDate>
                    <mainLanguageCode>eng-GB</mainLanguageCode>
                    <currentVersionNo>1</currentVersionNo>
                    <alwaysAvailable>false</alwaysAvailable>
                    <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/59/objectstates"/>
                </Content>
            </ContentInfo>
        </Location>
    </Bookmark>
    <Bookmark media-type="application/vnd.ez.api.Bookmark+xml" _href="/api/ezp/v2/bookmark/56">
        <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/56">
            <id>56</id>
            <priority>0</priority>
            <hidden>false</hidden>
            <invisible>false</invisible>
            <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2"/>
            <pathString>/1/2/56/</pathString>
            <depth>2</depth>
            <childCount>0</childCount>
            <remoteId>4e83abdb00439c7383517126ea656631</remoteId>
            <Children media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/2/56/children"/>
            <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/55"/>
            <sortField>NAME</sortField>
            <sortOrder>ASC</sortOrder>
            <UrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/locations/1/2/56/urlaliases"/>
            <ContentInfo media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/55">
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/55" remoteId="02c379510a48965f8253af461079b7fe" id="55">
                    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
                    <Name>111</Name>
                    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/55/versions"/>
                    <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/55/currentversion"/>
                    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
                    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/55/locations"/>
                    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                    <lastModificationDate>2018-11-08T12:03:34+01:00</lastModificationDate>
                    <publishedDate>2018-11-08T12:03:34+01:00</publishedDate>
                    <mainLanguageCode>eng-GB</mainLanguageCode>
                    <currentVersionNo>1</currentVersionNo>
                    <alwaysAvailable>false</alwaysAvailable>
                    <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/55/objectstates"/>
                </Content>
            </ContentInfo>
        </Location>
    </Bookmark>
</BookmarkList>
```

##### application/vnd.ez.api.BookmarkList+json

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | BookmarkList   | 

```json
{
    "BookmarkList": {
        "_media-type": "application/vnd.ez.api.BookmarkList+json",
        "count": 1,
        "items": [
            {
                "_media-type": "application/vnd.ez.api.Bookmark+json",
                "__href": "/api/ezp/v2/bookmark/2",
                "Location": {
                    "_media-type": "application/vnd.ez.api.Location+json",
                    "_href": "/api/ezp/v2/content/locations/1/2",
                    "id": 2,
                    "priority": 0,
                    "hidden": false,
                    "invisible": false,
                    "ParentLocation": {
                        "_media-type": "application/vnd.ez.api.Location+json",
                        "_href": "/api/ezp/v2/content/locations/1"
                    },
                    "pathString": "/1/2/",
                    "depth": 1,
                    "childCount": 4,
                    "remoteId": "f3e90596361e31d496d4026eb624c983",
                    "Children": {
                        "_media-type": "application/vnd.ez.api.LocationList+json",
                        "_href": "/api/ezp/v2/content/locations/1/2/children"
                    },
                    "Content": {
                        "_media-type": "application/vnd.ez.api.Content+json",
                        "_href": "/api/ezp/v2/content/objects/1"
                    },
                    "sortField": "PRIORITY",
                    "sortOrder": "ASC",
                    "UrlAliases": {
                        "_media-type": "application/vnd.ez.api.UrlAliasRefList+json",
                        "_href": "/api/ezp/v2/content/locations/1/2/urlaliases"
                    },
                    "ContentInfo": {
                        "_media-type": "application/vnd.ez.api.ContentInfo+json",
                        "_href": "/api/ezp/v2/content/objects/1",
                        "Content": {
                            "_media-type": "application/vnd.ez.api.ContentInfo+json",
                            "_href": "/api/ezp/v2/content/objects/1",
                            "_remoteId": "9459d3c29e15006e45197295722c7ade",
                            "_id": 1,
                            "ContentType": {
                                "_media-type": "application/vnd.ez.api.ContentType+json",
                                "_href": "/api/ezp/v2/content/types/1"
                            },
                            "Name": "eZ Platform",
                            "Versions": {
                                "_media-type": "application/vnd.ez.api.VersionList+json",
                                "_href": "/api/ezp/v2/content/objects/1/versions"
                            },
                            "CurrentVersion": {
                                "_media-type": "application/vnd.ez.api.Version+json",
                                "_href": "/api/ezp/v2/content/objects/1/currentversion"
                            },
                            "Section": {
                                "_media-type": "application/vnd.ez.api.Section+json",
                                "_href": "/api/ezp/v2/content/sections/1"
                            },
                            "Locations": {
                                "_media-type": "application/vnd.ez.api.LocationList+json",
                                "_href": "/api/ezp/v2/content/objects/1/locations"
                            },
                            "Owner": {
                                "_media-type": "application/vnd.ez.api.User+json",
                                "_href": "/api/ezp/v2/user/users/14"
                            },
                            "lastModificationDate": "2015-11-30T13:10:46+00:00",
                            "publishedDate": "2015-11-30T13:10:46+00:00",
                            "mainLanguageCode": "eng-GB",
                            "currentVersionNo": 9,
                            "alwaysAvailable": true,
                            "ObjectStates": {
                                "_media-type": "application/vnd.ez.api.ContentObjectStates+json",
                                "_href": "/api/ezp/v2/content/objects/1/objectstates"
                            }
                        }
                    }
                }
            }
        ]
    }
}
```

##### 401

Error - the user is not authorized to list bookmarks

### Create bookmark

Add given Location to bookmarks of current user

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/bookmark/{locationId}`   | 
| Method                     | POST                       | 

#### Responses

##### 201

Created

##### 401

Error - the user is not authorized to given location

##### 404

Error - a given Location not exists

##### 409

Error - Location is already bookmarked

### Check if location is bookmarked

Check if given Location is bookmarked by current user

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/bookmark/{locationId}`   | 
| Method                     | HEAD                       | 

#### Responses

##### 200

OK - bookmarked

##### 401

Error - the user is not authorized to given location

##### 404

Error - a given Location not exists / is not bookmarked

### Delete bookmark

Delete given Location from bookmarks of current user

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/bookmark/{locationId}`   | 
| Method                     | DELETE                     | 

#### Responses

##### 204

Deleted - no content

##### 401

Error - the user is not authorized to given location

##### 404

Error - a given Location not exists / is not bookmarked

## Managing content

### Creating Content

Creates a new content draft assigned to the authenticated user. If a different userId is given in the input it is assigned to the given user but this required special rights for the authenticated user (this is useful for content staging where the transfer process does not have to authenticate with the user which created the content object in the source server). The user has to publish the content if it should be visible.

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| URI                  | `/content/objects`   | 
| Method               | POST                 | 

#### Headers

##### Accept

Content - if set all informations for the content object including the embedded current version are returned in XML or JSON format. ContentInfo - if set all informations for the content object (excluding the current version) are returned in XML or JSON format

| Parameter                                                                                                                                                                      | Value                                                                                                                                                                          | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | 
| Type                                                                                                                                                                           | string                                                                                                                                                                         | 
| Default                                                                                                                                                                        | n/a                                                                                                                                                                            | 
| Required                                                                                                                                                                       | no                                                                                                                                                                             | 
| Example                                                                                                                                                                        | `application/vnd.ez.api.Content+xml`<br>`application/vnd.ez.api.Content+json`<br>`application/vnd.ez.api.ContentInfo+xml`<br>`application/vnd.ez.api.ContentInfo+json`<br>``   | 

##### Content-Type

The ContentCreate schema encoded in XML or JSON

| Parameter                                                                                         | Value                                                                                             | 
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | 
| Type                                                                                              | string                                                                                            | 
| Default                                                                                           | n/a                                                                                               | 
| Required                                                                                          | no                                                                                                | 
| Example                                                                                           | `application/vnd.ez.api.ContentCreate+xml`<br>`application/vnd.ez.api.ContentCreate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.ContentCreate+xml

| Parameter       | Value           | 
| --------------- | --------------- | 
| Type            | ContentCreate   | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.Content+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Content     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/83" remoteId="a9c8f00b1dba880df7a5ed3e93fad421" id="83">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
    <Name>draft article</Name>
    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/83/versions"/>
    <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/83/currentversion">
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/83/versions/1">
            <VersionInfo>
                <id>547</id>
                <versionNo>1</versionNo>
                <status>DRAFT</status>
                <modificationDate>2019-02-19T15:55:37+01:00</modificationDate>
                <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                <creationDate>2019-02-19T15:55:37+01:00</creationDate>
                <initialLanguageCode>eng-GB</initialLanguageCode>
                <languageCodes>eng-GB</languageCodes>
                <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                    <Language>
                        <languageCode>eng-GB</languageCode>
                    </Language>
                </VersionTranslationInfo>
                <names>
                    <value languageCode="eng-GB">draft article</value>
                </names>
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/83"/>
            </VersionInfo>
            <Fields>
                <field>
                    <id>446</id>
                    <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>draft article</fieldValue>
                </field>
                <field>
                    <id>447</id>
                    <fieldDefinitionIdentifier>short_title</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue/>
                </field>
                <field>
                    <id>448</id>
                    <fieldDefinitionIdentifier>author</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezauthor</fieldTypeIdentifier>
                    <fieldValue/>
                </field>
                <field>
                    <id>449</id>
                    <fieldDefinitionIdentifier>intro</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;draft draft&lt;/para&gt;&lt;/section&gt;
</value>
                        <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;draft draft&lt;/p&gt;&lt;/section&gt;
</value>
                    </fieldValue>
                </field>
                <field>
                    <id>450</id>
                    <fieldDefinitionIdentifier>body</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;draft draft draft &lt;/para&gt;&lt;/section&gt;
</value>
                        <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;draft draft draft &lt;/p&gt;&lt;/section&gt;
</value>
                    </fieldValue>
                </field>
                <field>
                    <id>451</id>
                    <fieldDefinitionIdentifier>enable_comments</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezboolean</fieldTypeIdentifier>
                    <fieldValue>false</fieldValue>
                </field>
                <field>
                    <id>452</id>
                    <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezobjectrelation</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="destinationContentId"/>
                    </fieldValue>
                </field>
            </Fields>
            <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/83/versions/1/relations"/>
        </Version>
    </CurrentVersion>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/83/locations"/>
    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <currentVersionNo>1</currentVersionNo>
    <alwaysAvailable>true</alwaysAvailable>
    <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/83/objectstates"/>
</Content>
```

##### application/vnd.ez.api.ContentInfo+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentInfo   | 

##### 400

Error - the Input does not match the input schema definition or the validation on a field fails

##### 401

Error - the user is not authorized to create this object in this location

##### 404

Error - a parent Location is specified in the request body and it does not exist

### Load Content by remote id

Loads the content for a given remote ID

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| URI                  | `/content/objects`   | 
| Method               | GET                  | 

#### Query Parameters

| Name                                                                                        | Type                                                                                        | Default                                                                                     | Required                                                                                    | Example                                                                                     | Description                                                                                 | 
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | 
| remoteId                                                                                    | string                                                                                      | n/a                                                                                         | no                                                                                          | n/a                                                                                         | The remote ID of the content. If present the content with the given remote ID is returned   | 

#### Responses

##### 307

Temporary Redirect

##### 404

Error - the content with the given remote ID does not exist

### Load Content

Loads the Content Object for the given ID. Depending on the Accept header the current version is embedded (i.e the current published version or if not exists the draft of the authenticated user)

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/objects/{contentId}`   | 
| Method                           | GET                              | 

#### Headers

##### Accept

Content - 	if set all informations for the content object including the embedded current version are returned in XML or JSON format. ContentInfo - if set all informations for the content object (excluding the current version) are returned in XML or JSON format

| Parameter                                                                                                                                                                      | Value                                                                                                                                                                          | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | 
| Type                                                                                                                                                                           | string                                                                                                                                                                         | 
| Default                                                                                                                                                                        | n/a                                                                                                                                                                            | 
| Required                                                                                                                                                                       | no                                                                                                                                                                             | 
| Example                                                                                                                                                                        | `application/vnd.ez.api.Content+xml`<br>`application/vnd.ez.api.Content+json`<br>`application/vnd.ez.api.ContentInfo+xml`<br>`application/vnd.ez.api.ContentInfo+json`<br>``   | 

##### If-None-Match

If the provided ETag matches the current ETag then a "304 Not Modified" is returned. The ETag changes if the meta data was changed - this happens also if there is a new published version.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | `ETag`      | 

#### Query Parameters

| Name                                                                                       | Type                                                                                       | Default                                                                                    | Required                                                                                   | Example                                                                                    | Description                                                                                | 
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | 
| languages                                                                                  | string                                                                                     | n/a                                                                                        | no                                                                                         | n/a                                                                                        | Restricts the output of translatable fields to the given languages. Comma separated list   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Content+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Content     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/54" remoteId="d2b6b7f5d0935c45456a80d3a154f2e7" id="54">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
    <Name>test</Name>
    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/54/versions"/>
    <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/54/currentversion">
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/54/versions/1">
            <VersionInfo>
                <id>515</id>
                <versionNo>1</versionNo>
                <status>PUBLISHED</status>
                <modificationDate>2018-09-27T13:31:25+02:00</modificationDate>
                <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                <creationDate>2018-09-27T13:31:24+02:00</creationDate>
                <initialLanguageCode>eng-GB</initialLanguageCode>
                <languageCodes>eng-GB</languageCodes>
                <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                    <Language>
                        <languageCode>eng-GB</languageCode>
                    </Language>
                </VersionTranslationInfo>
                <names>
                    <value languageCode="eng-GB">test</value>
                </names>
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/54"/>
            </VersionInfo>
            <Fields>
                <field>
                    <id>249</id>
                    <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>test</fieldValue>
                </field>
                <field>
                    <id>250</id>
                    <fieldDefinitionIdentifier>short_title</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>test</fieldValue>
                </field>
                <field>
                    <id>251</id>
                    <fieldDefinitionIdentifier>author</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezauthor</fieldTypeIdentifier>
                    <fieldValue>
                        <value>
                            <value key="id">1</value>
                            <value key="name">Administrator User</value>
                            <value key="email">nospam@ez.no</value>
                        </value>
                    </fieldValue>
                </field>
                <field>
                    <id>252</id>
                    <fieldDefinitionIdentifier>intro</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.&lt;/para&gt;&lt;/section&gt;
</value>
                        <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.&lt;/p&gt;&lt;/section&gt;
</value>
                    </fieldValue>
                </field>
                <field>
                    <id>253</id>
                    <fieldDefinitionIdentifier>body</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; version=&quot;5.0-variant ezpublish-1.0&quot;/&gt;
</value>
                        <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;/&gt;
</value>
                    </fieldValue>
                </field>
                <field>
                    <id>254</id>
                    <fieldDefinitionIdentifier>enable_comments</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezboolean</fieldTypeIdentifier>
                    <fieldValue>false</fieldValue>
                </field>
                <field>
                    <id>255</id>
                    <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezobjectrelation</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="destinationContentId"/>
                    </fieldValue>
                </field>
            </Fields>
            <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/54/versions/1/relations"/>
        </Version>
    </CurrentVersion>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
    <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/55"/>
    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/54/locations"/>
    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <lastModificationDate>2018-09-27T13:31:25+02:00</lastModificationDate>
    <publishedDate>2018-09-27T13:31:25+02:00</publishedDate>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <currentVersionNo>1</currentVersionNo>
    <alwaysAvailable>false</alwaysAvailable>
    <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/54/objectstates"/>
</Content>
```

##### application/vnd.ez.api.ContentInfo+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentInfo   | 

##### 401

Error - the user is not authorized to read this object. This could also happen if there is no published version yet and another user owns a draft of this content

##### 404

Error - the ID is not found

### Update Content

This method updates the content metadata which is independent from a version. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/objects/{contentId}`   | 
| Method                           | PATCH                            | 

#### Headers

##### Accept

If set all informations for the content object (excluding the current version) are returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.ContentInfo+xml`<br>`application/vnd.ez.api.ContentInfo+json`<br>``   | 

##### If-match

Causes to patch only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | `ETag`      | 

##### Content-Type

The ContentUpdate schema encoded in XML or JSON

| Parameter                                                                                         | Value                                                                                             | 
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | 
| Type                                                                                              | string                                                                                            | 
| Default                                                                                           | n/a                                                                                               | 
| Required                                                                                          | no                                                                                                | 
| Example                                                                                           | `application/vnd.ez.api.ContentUpdate+xml`<br>`application/vnd.ez.api.ContentUpdate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.ContentUpdate+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentInfo   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.ContentInfo+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentInfo   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/80" remoteId="69848aeb86164c35e5c98202eebe9e05" id="80">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
    <Name>article1</Name>
    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/80/versions"/>
    <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/80/currentversion"/>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
    <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/63/66"/>
    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/80/locations"/>
    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/11"/>
    <lastModificationDate>2019-02-19T15:00:34+01:00</lastModificationDate>
    <publishedDate>2019-02-19T15:00:34+01:00</publishedDate>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <currentVersionNo>1</currentVersionNo>
    <alwaysAvailable>false</alwaysAvailable>
    <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/80/objectstates"/>
</Content>
```

##### 400

Error - the Input does not match the input schema definition

##### 401

Error - the user is not authorized to update this object

##### 404

Error - the content ID does not exist

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

##### 415

Error - the media-type is not one of those specified in headers

### Delete Content

The content is deleted. If the content has locations (which is required in 4.x) on delete all locations assigned the content object are deleted via delete subtree.

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/objects/{contentId}`   | 
| Method                           | DELETE                           | 

#### Responses

##### 204

The content is deleted.

##### 404

Error - content object was not found

##### 401

Error - the user is not authorized to delete this object

### Copy content

Creates a new content object as copy under the given parent Location given in the destination header. COPY or POST with header X-HTTP-Method-Override COPY.

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/objects/{contentId}`   | 
| Method                           | COPY                             | 

#### Headers

##### destination

A Location resource to which the content object should be copied.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 201

Copy created

##### 401

Error - the user is not authorized to copy this object to the given location

##### 404

Error - the source or destination resource do not exist.

### Delete (permanently) Translation from all Versions of a Content

Permanently delete a Translation from all Versions of a Content

| Parameter                                                    | Value                                                        | 
| ------------------------------------------------------------ | ------------------------------------------------------------ | 
| URI                                                          | `/content/objects/{contentId}/translations/{languageCode}`   | 
| Method                                                       | DELETE                                                       | 

#### Responses

##### 204

No Content

##### 401

Error - the user is not authorized to delete Content (content/remove policy)

##### 404

Error - the Content item was not found

##### 406

Error - the given Translation does not exist for the Content

##### 409

Error - the specified Translation is the only one any Version has or is the Main Translation

### Get Current Version

Redirects to the current version of the content object

| Parameter                                       | Value                                           | 
| ----------------------------------------------- | ----------------------------------------------- | 
| URI                                             | `/content/objects/{contentId}/currentversion`   | 
| Method                                          | GET                                             | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Version+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Version     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/4">
    <VersionInfo>
        <id>551</id>
        <versionNo>4</versionNo>
        <status>PUBLISHED</status>
        <modificationDate>2019-02-20T11:32:12+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <creationDate>2019-02-20T11:32:06+01:00</creationDate>
        <initialLanguageCode>eng-GB</initialLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
            <Language>
                <languageCode>eng-GB</languageCode>
            </Language>
        </VersionTranslationInfo>
        <names>
            <value languageCode="eng-GB">7777</value>
        </names>
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
    </VersionInfo>
    <Fields>
        <field>
            <id>298</id>
            <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>New article 7</fieldValue>
        </field>
        <field>
            <id>299</id>
            <fieldDefinitionIdentifier>short_title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>7777</fieldValue>
        </field>
        <field>
            <id>300</id>
            <fieldDefinitionIdentifier>author</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezauthor</fieldTypeIdentifier>
            <fieldValue>
                <value>
                    <value key="id">1</value>
                    <value key="name">7777</value>
                    <value key="email"></value>
                </value>
            </fieldValue>
        </field>
        <field>
            <id>301</id>
            <fieldDefinitionIdentifier>intro</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;777777777777788880000&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;777777777777788880000&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>302</id>
            <fieldDefinitionIdentifier>body</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;88888888888&lt;/para&gt;&lt;para&gt;0000&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;88888888888&lt;/p&gt;&lt;p&gt;0000&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>303</id>
            <fieldDefinitionIdentifier>enable_comments</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezboolean</fieldTypeIdentifier>
            <fieldValue>false</fieldValue>
        </field>
        <field>
            <id>304</id>
            <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezobjectrelation</fieldTypeIdentifier>
            <fieldValue>
                <value key="destinationContentId"/>
            </fieldValue>
        </field>
    </Fields>
    <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/61/versions/4/relations"/>
</Version>
```

##### 307

Temporary redirect

##### 404

Error - the resource does not exist

### Create a Draft from current Version

The system creates a new draft version as a copy from the current version. COPY or POST with header X-HTTP-Method-Override COPY.

| Parameter                                       | Value                                           | 
| ----------------------------------------------- | ----------------------------------------------- | 
| URI                                             | `/content/objects/{contentId}/currentversion`   | 
| Method                                          | COPY                                            | 

#### Headers

##### Accept

If set the updated version is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Version+xml`<br>`application/vnd.ez.api.Version+json`<br>``   | 

#### Responses

##### 201

Created

###### Payload

##### application/vnd.ez.api.Version+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Version     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/6">
    <VersionInfo>
        <id>553</id>
        <versionNo>6</versionNo>
        <status>DRAFT</status>
        <modificationDate>2019-02-20T12:35:10+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <creationDate>2019-02-20T12:35:10+01:00</creationDate>
        <initialLanguageCode>eng-GB</initialLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
            <Language>
                <languageCode>eng-GB</languageCode>
            </Language>
        </VersionTranslationInfo>
        <names>
            <value languageCode="eng-GB">7777</value>
        </names>
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
    </VersionInfo>
    <Fields>
        <field>
            <id>298</id>
            <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>New article 7</fieldValue>
        </field>
        <field>
            <id>299</id>
            <fieldDefinitionIdentifier>short_title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>7777</fieldValue>
        </field>
        <field>
            <id>300</id>
            <fieldDefinitionIdentifier>author</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezauthor</fieldTypeIdentifier>
            <fieldValue>
                <value>
                    <value key="id">1</value>
                    <value key="name">7777</value>
                    <value key="email"></value>
                </value>
            </fieldValue>
        </field>
        <field>
            <id>301</id>
            <fieldDefinitionIdentifier>intro</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;777777777777788880000&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;777777777777788880000&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>302</id>
            <fieldDefinitionIdentifier>body</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;88888888888&lt;/para&gt;&lt;para&gt;0000&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;88888888888&lt;/p&gt;&lt;p&gt;0000&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>303</id>
            <fieldDefinitionIdentifier>enable_comments</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezboolean</fieldTypeIdentifier>
            <fieldValue>false</fieldValue>
        </field>
        <field>
            <id>304</id>
            <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezobjectrelation</fieldTypeIdentifier>
            <fieldValue>
                <value key="destinationContentId"/>
            </fieldValue>
        </field>
    </Fields>
    <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/61/versions/6/relations"/>
</Version>
```

##### 401

Error - the user is not authorized to update this object

##### 403

Error - the current version is already a draft

##### 404

Error - the content object was not found

### List Versions

Returns a list of all versions of the content. This method does not include fields and relations in the Version elements of the response.

| Parameter                                 | Value                                     | 
| ----------------------------------------- | ----------------------------------------- | 
| URI                                       | `/content/objects/{contentId}/versions`   | 
| Method                                    | GET                                       | 

#### Headers

##### Accept

If set the version list is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.VersionList+xml`<br>`application/vnd.ez.api.VersionList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.VersionList+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | VersionList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<VersionList media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/61/versions">
    <VersionItem>
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/1"/>
        <VersionInfo>
            <id>522</id>
            <versionNo>1</versionNo>
            <status>ARCHIVED</status>
            <modificationDate>2019-02-20T11:30:15+01:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2018-11-09T14:50:16+01:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">777</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        </VersionInfo>
    </VersionItem>
    <VersionItem>
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/2"/>
        <VersionInfo>
            <id>543</id>
            <versionNo>2</versionNo>
            <status>ARCHIVED</status>
            <modificationDate>2019-02-20T11:31:52+01:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2019-02-19T14:59:15+01:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">777</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        </VersionInfo>
    </VersionItem>
    <VersionItem>
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/3"/>
        <VersionInfo>
            <id>550</id>
            <versionNo>3</versionNo>
            <status>ARCHIVED</status>
            <modificationDate>2019-02-20T11:32:12+01:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2019-02-20T11:31:34+01:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">7777</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        </VersionInfo>
    </VersionItem>
    <VersionItem>
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/4"/>
        <VersionInfo>
            <id>551</id>
            <versionNo>4</versionNo>
            <status>PUBLISHED</status>
            <modificationDate>2019-02-20T11:32:12+01:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2019-02-20T11:32:06+01:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">7777</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        </VersionInfo>
    </VersionItem>
</VersionList>
```

##### 401

Error - the user has no permission to read the versions

### Load Version

Loads a specific version of a content object. This method returns fields and relations

| Parameter                                             | Value                                                 | 
| ----------------------------------------------------- | ----------------------------------------------------- | 
| URI                                                   | `/content/objects/{contentId}/versions/{versionNo}`   | 
| Method                                                | GET                                                   | 

#### Headers

##### If-None-Match

Only return the version if the given ETag is the not current one otherwise a 304 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | `ETag`      | 

##### Accept

If set the version list is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Version+xml`<br>`application/vnd.ez.api.Version+json`<br>``   | 

#### Query Parameters

| Name                                                                                       | Type                                                                                       | Default                                                                                    | Required                                                                                   | Example                                                                                    | Description                                                                                | 
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | 
| fields                                                                                     | string                                                                                     | n/a                                                                                        | no                                                                                         | n/a                                                                                        | Fields which should be returned in the response. Comma separated list.                     | 
| responseGroups                                                                             | string                                                                                     | n/a                                                                                        | no                                                                                         | n/a                                                                                        | Alternative comma separated lists of predefined field groups                               | 
| languages                                                                                  | string                                                                                     | n/a                                                                                        | no                                                                                         | n/a                                                                                        | Restricts the output of translatable fields to the given languages. Comma separated list   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Version+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Version     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/3">
    <VersionInfo>
        <id>550</id>
        <versionNo>3</versionNo>
        <status>ARCHIVED</status>
        <modificationDate>2019-02-20T11:32:12+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <creationDate>2019-02-20T11:31:34+01:00</creationDate>
        <initialLanguageCode>eng-GB</initialLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
            <Language>
                <languageCode>eng-GB</languageCode>
            </Language>
        </VersionTranslationInfo>
        <names>
            <value languageCode="eng-GB">7777</value>
        </names>
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
    </VersionInfo>
    <Fields>
        <field>
            <id>298</id>
            <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>New article 77</fieldValue>
        </field>
        <field>
            <id>299</id>
            <fieldDefinitionIdentifier>short_title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>7777</fieldValue>
        </field>
        <field>
            <id>300</id>
            <fieldDefinitionIdentifier>author</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezauthor</fieldTypeIdentifier>
            <fieldValue>
                <value>
                    <value key="id">1</value>
                    <value key="name">7777</value>
                    <value key="email"></value>
                </value>
            </fieldValue>
        </field>
        <field>
            <id>301</id>
            <fieldDefinitionIdentifier>intro</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;777777777777788880000&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;777777777777788880000&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>302</id>
            <fieldDefinitionIdentifier>body</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;88888888888&lt;/para&gt;&lt;para&gt;0000&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;88888888888&lt;/p&gt;&lt;p&gt;0000&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>303</id>
            <fieldDefinitionIdentifier>enable_comments</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezboolean</fieldTypeIdentifier>
            <fieldValue>false</fieldValue>
        </field>
        <field>
            <id>304</id>
            <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezobjectrelation</fieldTypeIdentifier>
            <fieldValue>
                <value key="destinationContentId"/>
            </fieldValue>
        </field>
    </Fields>
    <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/61/versions/3/relations"/>
</Version>
```

##### 304

Error - the ETag does not match the current one

##### 401

Error - the user is not authorized to read this object

##### 404

Error - the ID or version is not found

### Update Version

A specific draft is updated. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                                             | Value                                                 | 
| ----------------------------------------------------- | ----------------------------------------------------- | 
| URI                                                   | `/content/objects/{contentId}/versions/{versionNo}`   | 
| Method                                                | PATCH                                                 | 

#### Headers

##### Accept

If set the updated version is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Version+xml`<br>`application/vnd.ez.api.Version+json`<br>``   | 

##### If-match

Causes to patch only if the specified ETag is the current one

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

##### Content-Type

The VersionUpdate schema encoded in XML or JSON

| Parameter                                                                                         | Value                                                                                             | 
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | 
| Type                                                                                              | string                                                                                            | 
| Default                                                                                           | n/a                                                                                               | 
| Required                                                                                          | no                                                                                                | 
| Example                                                                                           | `application/vnd.ez.api.VersionUpdate+xml`<br>`application/vnd.ez.api.VersionUpdate+json`<br>``   | 

#### Query Parameters

| Name                                                                                       | Type                                                                                       | Default                                                                                    | Required                                                                                   | Example                                                                                    | Description                                                                                | 
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | 
| languages                                                                                  | string                                                                                     | n/a                                                                                        | no                                                                                         | n/a                                                                                        | Restricts the output of translatable fields to the given languages. Comma separated list   | 

#### Payload

##### application/vnd.ez.api.VersionUpdate+xml

| Parameter       | Value           | 
| --------------- | --------------- | 
| Type            | VersionUpdate   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Version+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Version     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Version href="/content/objects/23/versions/4" media-type="application/vnd.ez.api.Version+xml">
  <VersionInfo>
    <id>45</id>
    <versionNo>4</versionNo>
    <status>DRAFT</status>
    <modificationDate>2012-02-20T12:00:00</modificationDate>
    <Creator href="/user/users/44" media-type="application/vnd.ez.api.User+xml" />
    <creationDate>22012-02-20T12:00:00</creationDate>
    <initialLanguageCode>ger-DE</initialLanguageCode>
    <names>
      <value languageCode="ger-DE">Neuer Titel</value>
    </names>
    <Content href="/content/objects/23" media-type="application/vnd.ez.api.ContentInfo+xml" />
  </VersionInfo>
  <Fields>
    <field>
      <id>1234</id>
      <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
      <languageCode>ger-DE</languageCode>
      <fieldValue>Neuer Titel</fieldValue>
    </field>
    <field>
      <id>1235</id>
      <fieldDefinitionIdentifier>summary</fieldDefinitionIdentifier>
      <languageCode>ger-DE</languageCode>
      <fieldValue>Dies ist eine neuse Zusammenfassungy</fieldValue>
    </field>
    <field>
      <fieldDefinitionIdentifier>authors</fieldDefinitionIdentifier>
      <languageCode>ger-DE</languageCode>
      <fieldValue>
        <authors>
          <author name="Klaus Mustermann" email="klaus.mustermann@example.net" />
        </authors>
      </fieldValue>
    </field>
  </Fields>
  <Relations>
    <Relation href="/content/object/32/versions/2/relations/43" media-type="application/vnd.ez.api.Relation+xml">
      <SourceContent href="/content/objects/23"
        media-type="application/vnd.ez.api.ContentInfo+xml" />
      <DestinationContent href="/content/objects/45"
        media-type="application/vnd.ez.api.ContentInfo+xml" />
      <RelationType>COMMON</RelationType>
    </Relation>
  </Relations>
</Version>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to update this version

##### 403

Error - the version is not allowed to change - i.e is not a DRAFT

##### 404

Error - the content ID or version ID does not exist

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

### Create a Draft from a Version

The system creates a new draft version as a copy from the given version. COPY or POST with header X-HTTP-Method-Override COPY.

| Parameter                                             | Value                                                 | 
| ----------------------------------------------------- | ----------------------------------------------------- | 
| URI                                                   | `/content/objects/{contentId}/versions/{versionNo}`   | 
| Method                                                | COPY                                                  | 

#### Headers

##### Accept

If set the updated version is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Version+xml`<br>`application/vnd.ez.api.Version+json`<br>``   | 

#### Responses

##### 201

Created

###### Payload

##### application/vnd.ez.api.Version+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Version     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/versions/6">
    <VersionInfo>
        <id>555</id>
        <versionNo>6</versionNo>
        <status>DRAFT</status>
        <modificationDate>2019-02-22T14:55:11+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <creationDate>2019-02-22T14:55:11+01:00</creationDate>
        <initialLanguageCode>eng-GB</initialLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
            <Language>
                <languageCode>eng-GB</languageCode>
            </Language>
        </VersionTranslationInfo>
        <names>
            <value languageCode="eng-GB">777</value>
        </names>
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
    </VersionInfo>
    <Fields>
        <field>
            <id>298</id>
            <fieldDefinitionIdentifier>title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>New article 7</fieldValue>
        </field>
        <field>
            <id>299</id>
            <fieldDefinitionIdentifier>short_title</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>777</fieldValue>
        </field>
        <field>
            <id>300</id>
            <fieldDefinitionIdentifier>author</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezauthor</fieldTypeIdentifier>
            <fieldValue>
                <value>
                    <value key="id">1</value>
                    <value key="name">7777</value>
                    <value key="email"></value>
                </value>
            </fieldValue>
        </field>
        <field>
            <id>301</id>
            <fieldDefinitionIdentifier>intro</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;77777777777778888&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;77777777777778888&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>302</id>
            <fieldDefinitionIdentifier>body</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezrichtext</fieldTypeIdentifier>
            <fieldValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; xmlns:ezxhtml=&quot;http://ez.no/xmlns/ezpublish/docbook/xhtml&quot; xmlns:ezcustom=&quot;http://ez.no/xmlns/ezpublish/docbook/custom&quot; version=&quot;5.0-variant ezpublish-1.0&quot;&gt;&lt;para&gt;88888888888&lt;/para&gt;&lt;/section&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;&gt;&lt;p&gt;88888888888&lt;/p&gt;&lt;/section&gt;
</value>
            </fieldValue>
        </field>
        <field>
            <id>303</id>
            <fieldDefinitionIdentifier>enable_comments</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezboolean</fieldTypeIdentifier>
            <fieldValue>false</fieldValue>
        </field>
        <field>
            <id>304</id>
            <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezobjectrelation</fieldTypeIdentifier>
            <fieldValue>
                <value key="destinationContentId"/>
            </fieldValue>
        </field>
    </Fields>
    <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/61/versions/6/relations"/>
</Version>
```

##### 401

Error - the user is not authorized to update this object

##### 404

Error - the content object was not found

### Delete Content Version

The version is deleted

| Parameter                                             | Value                                                 | 
| ----------------------------------------------------- | ----------------------------------------------------- | 
| URI                                                   | `/content/objects/{contentId}/versions/{versionNo}`   | 
| Method                                                | DELETE                                                | 

#### Responses

##### 204

No Content - the version is deleted

##### 404

Error - the content object or version nr was not found

##### 401

Error - the user is not authorized to delete this version

##### 403

Error - the version is in state published

### Publish a content version

The content version is published. PUBLISH or POST with header X-HTTP-Method-Override PUBLISH

| Parameter                                             | Value                                                 | 
| ----------------------------------------------------- | ----------------------------------------------------- | 
| URI                                                   | `/content/objects/{contentId}/versions/{versionNo}`   | 
| Method                                                | PUBLISH                                               | 

#### Responses

##### 204

No Content - the content version is published

##### 401

Error - the user is not authorized to publish this version

##### 403

Error - the version is not a draft

##### 404

Error - the content object or version nr was not found

### Delete Content Version Draft Translation

Removes a translation from a version draft

| Parameter                                                                         | Value                                                                             | 
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | 
| URI                                                                               | `/content/objects/{contentId}/versions/{versionNo}/translations/{languageCode}`   | 
| Method                                                                            | DELETE                                                                            | 

#### Responses

##### 204

No Content - removes a translation from a version draft

##### 401

Error - the user is not authorized to delete this translation

##### 403

Error - the version is in not draft state

##### 404

Error - the Content item or version number were not found

##### 406

Error - the given translation does not exist for the version

##### 409

Error - the specified translation is the only one the Version has or is the main translation

### Load relations of content

Loads the relations of the given version

| Parameter                                                       | Value                                                           | 
| --------------------------------------------------------------- | --------------------------------------------------------------- | 
| URI                                                             | `/content/objects/{contentId}/versions/{versionNo}/relations`   | 
| Method                                                          | GET                                                             | 

#### Headers

##### Accept

If set the relation is returned in XML or JSON format

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.RelationList+xml`<br>`application/vnd.ez.api.RelationList+json`<br>``   | 

#### Query Parameters

| Name                               | Type                               | Default                            | Required                           | Example                            | Description                        | 
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | 
| offset                             | integer                            | n/a                                | no                                 | n/a                                | The offset of the result set       | 
| limit                              | integer                            | n/a                                | no                                 | n/a                                | The number of bookmarks returned   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RelationList+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | RelationList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/61/versions/6/relations">
    <Relation media-type="application/vnd.ez.api.Relation+xml" href="/api/ezp/v2/content/objects/61/versions/6/relations/2">
        <SourceContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        <DestinationContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/86"/>
        <RelationType>COMMON</RelationType>
    </Relation>
    <Relation media-type="application/vnd.ez.api.Relation+xml" href="/api/ezp/v2/content/objects/61/versions/6/relations/3">
        <SourceContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        <DestinationContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61"/>
        <RelationType>COMMON</RelationType>
    </Relation>
</Relations>
```

##### 401

Error - the user is not authorized to read this object

##### 404

Error - the content object was not found

### Create a new Relation

Creates a new relation of type COMMON for the given draft.

| Parameter                                                       | Value                                                           | 
| --------------------------------------------------------------- | --------------------------------------------------------------- | 
| URI                                                             | `/content/objects/{contentId}/versions/{versionNo}/relations`   | 
| Method                                                          | POST                                                            | 

#### Headers

##### Accept

If set the updated version is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.Relation+xml`<br>`application/vnd.ez.api.Relation+json`<br>``   | 

##### Content-Type

The RelationCreate schema encoded in XML or JSON

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.RelationCreate+xml`<br>`application/vnd.ez.api.RelationCreate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.RelationCreate+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Relation    | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.Relation+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Relation    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Relation media-type="application/vnd.ez.api.Relation+xml" href="/api/ezp/v2/content/objects/86/versions/1/relations/1">
    <SourceContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/86"/>
    <DestinationContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/86"/>
    <RelationType>COMMON</RelationType>
</Relation>
```

### Load a relation

Loads a relation for the given content object

| Parameter                                                                    | Value                                                                        | 
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | 
| URI                                                                          | `/content/objects/{contentId}/versions/{versionNo}/relations/{relationId}`   | 
| Method                                                                       | GET                                                                          | 

#### Headers

##### Accept

If set the relation is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.Relation+xml`<br>`application/vnd.ez.api.Relation+json`<br>``   | 

#### Responses

##### 200

OK - loads a relation for the given content object

###### Payload

##### application/vnd.ez.api.Relation+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Relation    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Relation media-type="application/vnd.ez.api.Relation+xml" href="/api/ezp/v2/content/objects/86/versions/1/relations/1">
    <SourceContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/86"/>
    <DestinationContent media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/86"/>
    <RelationType>COMMON</RelationType>
</Relation>
```

##### 401

Error - the user is not authorized to read this object

##### 404

Error - the object with the given ID or the relation does not exist

### Delete a relation

Deletes a relation of the given draft.

| Parameter                                                                    | Value                                                                        | 
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | 
| URI                                                                          | `/content/objects/{contentId}/versions/{versionNo}/relations/{relationId}`   | 
| Method                                                                       | DELETE                                                                       | 

#### Responses

##### 204

No Content - deleted a relation of the given draft.

##### 401

Error - the user is not authorized to delete this relation

##### 403

Error - the relation is not of type COMMON or the given version is not a draft

##### 404

Error - content object was not found or the relation was not found in the given version

### Load relations of content

Redirects to the relations of the current version

| Parameter                                  | Value                                      | 
| ------------------------------------------ | ------------------------------------------ | 
| URI                                        | `/content/objects/{contentId}/relations`   | 
| Method                                     | GET                                        | 

#### Responses

##### 307

Temporary redirect

##### 401

Error - the user is not authorized to read this object

##### 404

Error - the content object was not found

### Create a new location for a content object

Creates a new Location for the given Content Object

| Parameter                                  | Value                                      | 
| ------------------------------------------ | ------------------------------------------ | 
| URI                                        | `/content/objects/{contentId}/locations`   | 
| Method                                     | POST                                       | 

#### Headers

##### Accept

If set the new Location is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.Location+xml`<br>`application/vnd.ez.api.Location+json`<br>``   | 

##### Content-Type

The LocationCreate schema encoded in XML or JSON

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.LocationCreate+json`<br>`application/vnd.ez.api.LocationCreate+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.LocationCreate+xml

| Parameter        | Value            | 
| ---------------- | ---------------- | 
| Type             | LocationCreate   | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.Location+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Location    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/42/69">
    <id>69</id>
    <priority>0</priority>
    <hidden>false</hidden>
    <invisible>false</invisible>
    <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/42"/>
    <pathString>/1/2/42/69/</pathString>
    <depth>3</depth>
    <childCount>0</childCount>
    <remoteId>0e8d6b87fe3b1588533b636a8549cc0c</remoteId>
    <Children media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/2/42/69/children"/>
    <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/61"/>
    <sortField>PATH</sortField>
    <sortOrder>ASC</sortOrder>
    <UrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/locations/1/2/42/69/urlaliases"/>
    <ContentInfo media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61">
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/61" remoteId="2c90ebb85a849a377a8df1ba775dbba4" id="61">
            <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/>
            <Name>7777</Name>
            <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/61/versions"/>
            <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/61/currentversion"/>
            <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
            <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/61/locations"/>
            <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <lastModificationDate>2019-02-22T15:01:46+01:00</lastModificationDate>
            <publishedDate>2018-11-09T14:50:16+01:00</publishedDate>
            <mainLanguageCode>eng-GB</mainLanguageCode>
            <currentVersionNo>5</currentVersionNo>
            <alwaysAvailable>false</alwaysAvailable>
            <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/61/objectstates"/>
        </Content>
    </ContentInfo>
</Location>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to create this location

##### 403

Error - a Location under the given parent ID already exists

### Get locations for a content object

Loads all locations for the given content object

| Parameter                                  | Value                                      | 
| ------------------------------------------ | ------------------------------------------ | 
| URI                                        | `/content/objects/{contentId}/locations`   | 
| Method                                     | GET                                        | 

#### Headers

##### Accept

If set the new Location is returned in XML or JSON format

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.LocationList+xml`<br>`application/vnd.ez.api.LocationList+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.LocationList+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | LocationList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<LocationList media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/61/locations">
    <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/62"/>
</LocationList>
```

##### 401

Error - the user is not authorized to read this object

##### 404

Error - the object with the given ID does not exist

### Get Object States of Content

Returns the Object States of a Content item

| Parameter                                     | Value                                         | 
| --------------------------------------------- | --------------------------------------------- | 
| URI                                           | `/content/objects/{contentId}/objectstates`   | 
| Method                                        | GET                                           | 

#### Headers

##### Accept

If set the Object State is returned in XML or JSON format

| Parameter                                                                                                     | Value                                                                                                         | 
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                          | string                                                                                                        | 
| Default                                                                                                       | n/a                                                                                                           | 
| Required                                                                                                      | no                                                                                                            | 
| Example                                                                                                       | `application/vnd.ez.api.ContentObjectStates+xml`<br>`application/vnd.ez.api.ContentObjectStates+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns the Object State

###### Payload

##### application/vnd.ez.api.ContentObjectStates+xml

| Parameter             | Value                 | 
| --------------------- | --------------------- | 
| Type                  | ContentObjectStates   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateList media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates">
    <ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates/1">
        <id>1</id>
        <identifier>not_locked</identifier>
        <priority>0</priority>
        <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2"/>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <names>
            <value languageCode="eng-GB">Not locked</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB"></value>
        </descriptions>
    </ObjectState>
    <ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates/4">
        <id>4</id>
        <identifier>old-state</identifier>
        <priority>1</priority>
        <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2"/>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <names>
            <value languageCode="eng-GB">New State</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB">New Object State</value>
        </descriptions>
    </ObjectState>
    <ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates/3">
        <id>3</id>
        <identifier>new-state</identifier>
        <priority>2</priority>
        <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2"/>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <names>
            <value languageCode="eng-GB">New State</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB">New Object State</value>
        </descriptions>
    </ObjectState>
    <ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates/2">
        <id>2</id>
        <identifier>locked</identifier>
        <priority>3</priority>
        <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2"/>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <names>
            <value languageCode="eng-GB">Locked</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB"></value>
        </descriptions>
    </ObjectState>
</ObjectStateList>
```

##### 404

Error - The Content item does not exist

### Set Object States of Content

Updates Object States of content. An Object State in the input overrides the state of the Object State Group. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                                     | Value                                         | 
| --------------------------------------------- | --------------------------------------------- | 
| URI                                           | `/content/objects/{contentId}/objectstates`   | 
| Method                                        | PATCH                                         | 

#### Headers

##### Accept

If set the updated Object State is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.ObjectState+xml`<br>`application/vnd.ez.api.ObjectState+json`<br>``   | 

##### Content-Type

The Content Object States input schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.ObjectStateUpdate+xml`<br>`application/vnd.ez.api.ObjectStateUpdate+json`<br>``   | 

##### If-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.ObjectState+xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | ObjectStateUpdate   | 

#### Responses

##### 204

OK - Object State updated

###### Payload

##### application/vnd.ez.api.ObjectState+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ObjectState   | 

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to set an Object State

##### 403

Error - The input contains multiple Object States of the same Object State Group

##### 412

Error - The current ETag does not match the one provided in the If-Match header

### List ObjectStateGroups

Returns a list of all Object State Groups

| Parameter                      | Value                          | 
| ------------------------------ | ------------------------------ | 
| URI                            | `/content/objectstategroups`   | 
| Method                         | GET                            | 

#### Headers

##### Accept

If set the Object State Group list is returned in XML or JSON format

| Parameter                                                                                                       | Value                                                                                                           | 
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                            | string                                                                                                          | 
| Default                                                                                                         | n/a                                                                                                             | 
| Required                                                                                                        | no                                                                                                              | 
| Example                                                                                                         | `application/vnd.ez.api.ObjectStateGroupList+xml`<br>`application/vnd.ez.api.ObjectStateGroupList+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns a list of Object State Groups

###### Payload

##### application/vnd.ez.api.ObjectStateGroupList+xml

| Parameter              | Value                  | 
| ---------------------- | ---------------------- | 
| Type                   | ObjectStateGroupList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateGroupList media-type="application/vnd.ez.api.ObjectStateGroupList+xml" href="/api/ezp/v2/content/objectstategroups">
    <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2">
        <id>2</id>
        <identifier>ez_lock</identifier>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <ObjectStates media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates"/>
        <names>
            <value languageCode="eng-GB">Lock</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB"></value>
        </descriptions>
    </ObjectStateGroup>
    <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/3">
        <id>3</id>
        <identifier>testgroup</identifier>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <ObjectStates media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/3/objectstates"/>
        <names>
            <value languageCode="eng-GB">Testgroup</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB"></value>
        </descriptions>
    </ObjectStateGroup>
</ObjectStateGroupList>
```

##### application/vnd.ez.api.ObjectStateGroupList+json

| Parameter              | Value                  | 
| ---------------------- | ---------------------- | 
| Type                   | ObjectStateGroupList   | 

##### 401

Error - The user has no permission to read Object State Groups

### Create ObjectStateGroup

Creates a new Object State Group

| Parameter                      | Value                          | 
| ------------------------------ | ------------------------------ | 
| URI                            | `/content/objectstategroups`   | 
| Method                         | POST                           | 

#### Headers

##### Accept

If set the new Object State Group is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.ObjectStateGroup+xml`<br>`application/vnd.ez.api.ObjectStateGroup+json`<br>``   | 

##### Content-Type

The ObjectStateGroup input schema encoded in XML or JSON

| Parameter                                                                                                           | Value                                                                                                               | 
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                | string                                                                                                              | 
| Default                                                                                                             | n/a                                                                                                                 | 
| Required                                                                                                            | no                                                                                                                  | 
| Example                                                                                                             | `application/vnd.ez.api.ObjectStateGroupCreate+json`<br>`application/vnd.ez.api.ObjectStateGroupCreate+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.ObjectStateGroupCreate+xml

| Parameter                | Value                    | 
| ------------------------ | ------------------------ | 
| Type                     | ObjectStateGroupCreate   | 

##### application/vnd.ez.api.ObjectStateGroupCreate+json

| Parameter                | Value                    | 
| ------------------------ | ------------------------ | 
| Type                     | ObjectStateGroupCreate   | 

#### Responses

##### 201

Object State Group created

###### Payload

##### application/vnd.ez.api.ObjectStateGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ObjectStateGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/6">
    <id>6</id>
    <identifier>custom-states</identifier>
    <defaultLanguageCode>eng-GB</defaultLanguageCode>
    <languageCodes>eng-GB</languageCodes>
    <ObjectStates media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/6/objectstates"/>
    <names>
        <value languageCode="eng-GB">Custom State</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">Custom Object state</value>
    </descriptions>
</ObjectStateGroup>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create an Object State Group

##### 403

Error - An Object State Group with same identifier already exists

### Get ObjectStateGroup

Returns the Object State Group with the provided ID

| Parameter                                           | Value                                               | 
| --------------------------------------------------- | --------------------------------------------------- | 
| URI                                                 | `/content/objectstategroups/{objectStateGroupId}`   | 
| Method                                              | GET                                                 | 

#### Headers

##### Accept

If set the Object State Group is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.ObjectStateGroup+xml`<br>`application/vnd.ez.api.ObjectStateGroup+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns the Object State Group

###### Payload

##### application/vnd.ez.api.ObjectStateGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ObjectStateGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/6">
    <id>6</id>
    <identifier>custom-states</identifier>
    <defaultLanguageCode>eng-GB</defaultLanguageCode>
    <languageCodes>eng-GB</languageCodes>
    <ObjectStates media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/6/objectstates"/>
    <names>
        <value languageCode="eng-GB">Custom State</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">Custom Object state</value>
    </descriptions>
</ObjectStateGroup>
```

##### application/vnd.ez.api.ObjectStateGroup+json

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ObjectStateGroup   | 

##### 401

Error - The user is not authorized to read Object State Groups

##### 404

Error - The Object State Group does not exist

### Update ObjectStateGroup

Updates an Object State Group. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                                           | Value                                               | 
| --------------------------------------------------- | --------------------------------------------------- | 
| URI                                                 | `/content/objectstategroups/{objectStateGroupId}`   | 
| Method                                              | PATCH                                               | 

#### Headers

##### Accept

If set the updated Object State Group is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.ObjectStateGroup+xml`<br>`application/vnd.ez.api.ObjectStateGroup+json`<br>``   | 

##### Content-Type

The ObjectStateGroup input schema encoded in XML or JSON

| Parameter                                                                                                           | Value                                                                                                               | 
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                | string                                                                                                              | 
| Default                                                                                                             | n/a                                                                                                                 | 
| Required                                                                                                            | no                                                                                                                  | 
| Example                                                                                                             | `application/vnd.ez.api.ObjectStateGroupUpdate+json`<br>`application/vnd.ez.api.ObjectStateGroupUpdate+xml`<br>``   | 

##### If-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.ObjectStateGroupUpdate+xml

| Parameter                | Value                    | 
| ------------------------ | ------------------------ | 
| Type                     | ObjectStateGroupUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateGroup>
    <names>
        <value languageCode="eng-GB">New Custom State name</value>
    </names>
</ObjectStateGroup>
```

#### Responses

##### 200

OK - Object Stated group updated

###### Payload

##### application/vnd.ez.api.ObjectStateGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ObjectStateGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/6">
    <id>6</id>
    <identifier>custom-states</identifier>
    <defaultLanguageCode>eng-GB</defaultLanguageCode>
    <languageCodes>eng-GB</languageCodes>
    <ObjectStates media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/6/objectstates"/>
    <names>
        <value languageCode="eng-GB">New Custom State name</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">Custom Object state</value>
    </descriptions>
</ObjectStateGroup>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to update an Object State Group

##### 403

Error - An Object State Group with the provided new identifier already exists

##### 412

Error - The current ETag does not match the one provided in the If-Match header

### Delete Object State Group

Deletes the given Object State Group including Object States

| Parameter                                           | Value                                               | 
| --------------------------------------------------- | --------------------------------------------------- | 
| URI                                                 | `/content/objectstategroups/{objectStateGroupId}`   | 
| Method                                              | DELETE                                              | 

#### Responses

##### 204

No Content - Object State Group deleted

##### 401

Error - The user is not authorized to delete an Object State Group

##### 404

Error - The Object State Group does not exist

### List Object States

Returns a list of all Object States of the given group

| Parameter                                                        | Value                                                            | 
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | 
| URI                                                              | `/content/objectstategroups/{objectStateGroupId}/objectstates`   | 
| Method                                                           | GET                                                              | 

#### Headers

##### Accept

If set the Object State list is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.ObjectStateList+xml`<br>`application/vnd.ez.api.ObjectStateList+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns a list of Object States

###### Payload

##### application/vnd.ez.api.ObjectStateList+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | ObjectStateList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateList media-type="application/vnd.ez.api.ObjectStateList+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates">
    <ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates/1">
        <id>1</id>
        <identifier>not_locked</identifier>
        <priority>0</priority>
        <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2"/>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <names>
            <value languageCode="eng-GB">Not locked</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB"></value>
        </descriptions>
    </ObjectState>
    <ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/2/objectstates/2">
        <id>2</id>
        <identifier>locked</identifier>
        <priority>1</priority>
        <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/2"/>
        <defaultLanguageCode>eng-GB</defaultLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <names>
            <value languageCode="eng-GB">Locked</value>
        </names>
        <descriptions>
            <value languageCode="eng-GB"></value>
        </descriptions>
    </ObjectState>
</ObjectStateList>
```

##### 401

Error - The user has no permission to read Object States

### Create Object State

Creates a new Object State

| Parameter                                                        | Value                                                            | 
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | 
| URI                                                              | `/content/objectstategroups/{objectStateGroupId}/objectstates`   | 
| Method                                                           | POST                                                             | 

#### Headers

##### Accept

If set the new Object State is returned in XML or JSON format

| Parameter                                                                          | Value                                                                              | 
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | 
| Type                                                                               | string                                                                             | 
| Default                                                                            | n/a                                                                                | 
| Required                                                                           | no                                                                                 | 
| Example                                                                            | `application/vnd.ez.api.ObjectState+xml application/vnd.ez.api.ObjectState+json`   | 

##### Content-Type

The Object State input schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.ObjectStateCreate+json`<br>`application/vnd.ez.api.ObjectStateCreate+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.ObjectStateCreate+xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | ObjectStateCreate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateCreate>
  <identifier>new-state</identifier>
  <priority>1</priority>
  <defaultLanguageCode>eng-GB</defaultLanguageCode>
  <names>
    <value languageCode="eng-GB">New State</value>
  </names>
  <descriptions>
    <value languageCode="eng-GB">New Object State</value>
  </descriptions>
</ObjectStateCreate>
```

#### Responses

##### 201

Object State created

###### Payload

##### application/vnd.ez.api.ObjectState+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ObjectState   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/6/objectstates/6">
    <id>6</id>
    <identifier>new-state</identifier>
    <priority>0</priority>
    <ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/6"/>
    <defaultLanguageCode>eng-GB</defaultLanguageCode>
    <languageCodes>eng-GB</languageCodes>
    <names>
        <value languageCode="eng-GB">New State</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">New Object State</value>
    </descriptions>
</ObjectState>
```

##### 400

Error - The input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create an Object State

##### 403

Error - An Object State with the same identifier already exists in the given group

### Get Object State

Returns the Object State

| Parameter                                                                        | Value                                                                            | 
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | 
| URI                                                                              | `/content/objectstategroups/{objectStateGroupId}/objectstates/{objectStateId}`   | 
| Method                                                                           | GET                                                                              | 

#### Headers

##### Accept

If set the Object State is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.ObjectState+xml`<br>`application/vnd.ez.api.ObjectState+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns the Object State

###### Payload

##### application/vnd.ez.api.ObjectState+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ObjectState   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectState media-type="application/vnd.ez.api.ObjectState+xml" href="/api/ezp/v2/content/objectstategroups/6/objectstates/2">
<id>2</id>
<identifier>locked</identifier>
<priority>1</priority>
<ObjectStateGroup media-type="application/vnd.ez.api.ObjectStateGroup+xml" href="/api/ezp/v2/content/objectstategroups/6"/>
<defaultLanguageCode>eng-GB</defaultLanguageCode>
<languageCodes>eng-GB</languageCodes>
<names>
    <value languageCode="eng-GB">Locked</value>
</names>
<descriptions>
    <value languageCode="eng-GB"></value>
</descriptions>
</ObjectState>
```

##### 401

Error - The user is not authorized to read Object State Groups

##### 404

Error - The Object State Group does not exist

### Update Object State

Updates an Object State. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                                                                        | Value                                                                            | 
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | 
| URI                                                                              | `/content/objectstategroups/{objectStateGroupId}/objectstates/{objectStateId}`   | 
| Method                                                                           | PATCH                                                                            | 

#### Headers

##### Accept

If set the updated Object State is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.ObjectState+xml`<br>`application/vnd.ez.api.ObjectState+json`<br>``   | 

##### Content-Type

The Object State input schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.ObjectStateUpdate+json`<br>`application/vnd.ez.api.ObjectStateUpdate+xml`<br>``   | 

##### If-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.ObjectStateUpdate+xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | ObjectStateUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ObjectStateCreate>
  <priority>3</priority>
  <defaultLanguageCode>eng-GB</defaultLanguageCode>
  <names>
    <value languageCode="eng-GB">New Object State name</value>
  </names>
</ObjectStateCreate>
```

#### Responses

##### 200

OK - Object State updated

###### Payload

##### application/vnd.ez.api.ObjectState+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ObjectState   | 

```xml
examples/content/objectstategroups/object_state_group_id/objectstates/object_state_id/PATCH/ObjectState.xml.example
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to update the Object State

##### 403

Error - An Object State with the given new identifier already exists in this group

##### 412

Error - The current ETag does not match the one provided in the If-Match header

### Delete Object State

Deletes provided Object State

| Parameter                                                                        | Value                                                                            | 
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | 
| URI                                                                              | `/content/objectstategroups/{objectStateGroupId}/objectstates/{objectStateId}`   | 
| Method                                                                           | DELETE                                                                           | 

#### Responses

##### 204

No Content - Object State deleted

##### 401

Error - The user is not authorized to delete an Object State Group

##### 404

Error - The Object State does not exist

### Load an image variation

Loads an image variation

| Parameter                                                             | Value                                                                 | 
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | 
| URI                                                                   | `/content/binary/images/{imageId}/variations/{variationIdentifier}`   | 
| Method                                                                | GET                                                                   | 

#### Headers

##### Accept

If set the image is returned in XML or JSON format

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.ImageVariation+xml`<br>`application/vnd.ez.api.ImageVariation+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.ImageVariation+xml

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| Type                    | ContentImageVariation   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentImageVariation media-type="application/vnd.ez.api.ContentImageVariation+xml" href="/api/ezp/v2/content/binary/images/61-216-1/variations/large">
    <uri>http://127.0.0.1:8000/var/site/storage/images/_aliases/large/6/1/2/0/216-1-eng-GB/ez-logo-small.png</uri>
    <contentType>image/png</contentType>
    <width>20</width>
    <height>20</height>
    <fileSize>1709</fileSize>
</ContentImageVariation>
```

##### 401

Error - the user is not authorized to read this object

##### 404

Error - imageId doesn't match any image OR variationIdentifier doesn't match any known variation

### Load locations by id/remoteId/urlAlias

Loads the Location for a given ID (x), remote ID or URL alias

| Parameter              | Value                  | 
| ---------------------- | ---------------------- | 
| URI                    | `/content/locations`   | 
| Method                 | GET                    | 

#### Query Parameters

| Name                                                                                                 | Type                                                                                                 | Default                                                                                              | Required                                                                                             | Example                                                                                              | Description                                                                                          | 
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | 
| id                                                                                                   | string                                                                                               | n/a                                                                                                  | no                                                                                                   | n/a                                                                                                  | The ID of the location. If present the Location is with the given ID is returned.                    | 
| remoteId                                                                                             | string                                                                                               | n/a                                                                                                  | no                                                                                                   | n/a                                                                                                  | The remoteId of the location. If present the Location with the given remoteId is returned            | 
| urlAlias                                                                                             | string                                                                                               | n/a                                                                                                  | no                                                                                                   | n/a                                                                                                  | One of the URL  Aliases of the location. If present the Location with given URL  Alias is returned   | 

#### Responses

##### 307

Temporary redirect to main resource URL.

##### 200

###### Payload

##### application/vnd.ez.api.LocationList+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Location    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<LocationList href="/content/objects/23/locations" media-type="application/vnd.ez.api.LocationList+xml">
  <Location href="/content/locations/1/2/56" media-type="application/vnd.ez.api.Location+xml"/>
  <Location href="/content/locations/1/4/73/133" media-type="application/vnd.ez.api.Location+xml"/>
</LocationList>
```

##### 404

Error - the Location with the given ID (remoteId or urlAlias) does not exist

### Load location

Loads the Location for the given path e.g. '/content/locations/1/2/61'

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/content/locations/{path}`   | 
| Method                        | GET                           | 

#### Headers

##### Accept

If set the new Location is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.Location+xml`<br>`application/vnd.ez.api.Location+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Location+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Location    | 

```xml
<?xml version="1.0" encoding="UTF-8"?> <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/61"> <id>61</id> <priority>0</priority> <hidden>false</hidden> <invisible>false</invisible> <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2"/> <pathString>/1/2/61/</pathString> <depth>2</depth> <childCount>0</childCount> <remoteId>2cfa66027e3806b113d994c9c26d3a66</remoteId> <Children media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/2/61/children"/> <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/60"/> <sortField>NAME</sortField> <sortOrder>ASC</sortOrder> <UrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/locations/1/2/61/urlaliases"/> <ContentInfo media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/60"> <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/60" remoteId="f9198276543bfe5e1dfc01a9a8d0c7ee" id="60"> <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2"/> <Name>666</Name> <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/60/versions"/> <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/60/currentversion"/> <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/> <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/60/locations"/> <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/> <lastModificationDate>2018-11-09T14:49:52+01:00</lastModificationDate> <publishedDate>2018-11-09T14:49:52+01:00</publishedDate> <mainLanguageCode>eng-GB</mainLanguageCode> <currentVersionNo>1</currentVersionNo> <alwaysAvailable>false</alwaysAvailable> <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/60/objectstates"/> </Content> </ContentInfo> </Location>
```

##### 401

Error - the user is not authorized to read this location

##### 404

Error - the Location with the given path does not exist

### Move Subtree

Moves the Location to another parent. The destination can also be /content/trash where the Location is put into the trash. (NOTE - Be aware that the user might not have access to the item any longer after it has been moved, for example when read access is limited by subtree). MOVE or POST with header X-HTTP-Method-Override MOVE

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/content/locations/{path}`   | 
| Method                        | MOVE                          | 

#### Headers

##### Destination

A parent Location resource to which the Location is moved e.g. '/api/ezp/v2/content/locations/1/63'

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 201

Created. If destination is /api/ezp/v2/content/trash and content only has one Location (NOTE Like on normal subtree moves, be aware that the user might not have access to the item any longer after it has been moved to trash)

##### 204

No Content. If destination is /api/ezp/v2/content/trash and content still has other locations (no trash item is created).

##### 401

Error - the user is not authorized to move this location

##### 404

Error - the Location with the given ID does not exist

### Copy Subtree

Copies the subtree to another parent. COPY or POST with header X-HTTP-Method-Override COPY

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/content/locations/{path}`   | 
| Method                        | COPY                          | 

#### Headers

##### Destination

A parent Location resource to which the Location is moved e.g. '/api/ezp/v2/content/locations/1/63'

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 201

Created. Copied the subtree to another parent.

##### 401

Error - the user is not authorized to move this location

##### 404

Error - the Location with the given ID does not exist

### Delete Subtree

Deletes the complete subtree for the given path. Every content object is deleted which does not have any other location. Otherwise the deleted Location is removed from the content object. The children are recursively deleted.

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/content/locations/{path}`   | 
| Method                        | DELETE                        | 

#### Responses

##### 204

No Content - deleted.

##### 401

Error - the user is not authorized to delete this subtree

##### 404

Error - the Location with the given ID does not exist

### Get child locations

Loads all child locations for the given parent location

| Parameter                              | Value                                  | 
| -------------------------------------- | -------------------------------------- | 
| URI                                    | `/content/locations/{path}/children`   | 
| Method                                 | GET                                    | 

#### Headers

##### Accept

If set the new Location list is returned in XML or JSON format

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.LocationList+xml`<br>`application/vnd.ez.api.LocationList+json`<br>``   | 

#### Query Parameters

| Name                               | Type                               | Default                            | Required                           | Example                            | Description                        | 
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | 
| offset                             | integer                            | n/a                                | no                                 | n/a                                | The offset of the result set       | 
| limit                              | integer                            | n/a                                | no                                 | n/a                                | The number of bookmarks returned   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.LocationList+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | LocationList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<LocationList media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/63/children">
    <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/63/60"/>
    <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/63/61"/>
    <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/63/62"/>
    <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/63/67"/>
</LocationList>
```

##### 401

Error - the user is not authorized to read this object

##### 404

Error - the object with the given ID does not exist

### List UrlAliases for location

Returns the list of URL aliases for a Location

| Parameter                                | Value                                    | 
| ---------------------------------------- | ---------------------------------------- | 
| URI                                      | `/content/locations/{path}/urlaliases`   | 
| Method                                   | GET                                      | 

#### Headers

##### Accept

If set the URL alias list contains only references and is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.UrlAliasRefList+xml`<br>`application/vnd.ez.api.UrlAliasRefList+json`<br>``   | 

#### Query Parameters

| Name                                                                                                      | Type                                                                                                      | Default                                                                                                   | Required                                                                                                  | Example                                                                                                   | Description                                                                                               | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| custom                                                                                                    | boolean                                                                                                   | n/a                                                                                                       | no                                                                                                        | n/a                                                                                                       | Indicates whether autogenerated (false) or manual URL aliases (true) should be returned (default true).   | 

#### Responses

##### 200

OK - returns the list of URL aliases

###### Payload

##### application/vnd.ez.api.UrlAliasRefList+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | UrlAliasRefList   | 

##### 400

Error - The user has no permission to read URL aliases

##### 401

Error - The Location was not found

### Update location

Updates the location, this method can also be used to hide/unhide a Location via the hidden field in the LocationUpdate. PATCH or POST with header X-HTTP-Method-Override PATCH

| Parameter                           | Value                               | 
| ----------------------------------- | ----------------------------------- | 
| URI                                 | `/content/locations/{locationId}`   | 
| Method                              | PATCH                               | 

#### Headers

##### Accept

If set the new Location is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.Location+xml`<br>`application/vnd.ez.api.Location+json`<br>``   | 

##### Content-Type

The LocationUpdate schema encoded in XML or JSON

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.LocationUpdate+xml`<br>`application/vnd.ez.api.LocationUpdate+json`<br>``   | 

##### If-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.LocationUpdate+xml

| Parameter              | Value                  | 
| ---------------------- | ---------------------- | 
| Type                   | LocationUpdateStruct   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<LocationUpdate>
  <priority>3</priority>
  <hidden>true</hidden>
  <remoteId>remoteId-qwert999</remoteId>
  <sortField>CLASS</sortField>
  <sortOrder>DESC</sortOrder>
</LocationUpdate>
```

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Location+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Location    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Location href="/content/locations/1/5/73/133" media-type="application/vnd.ez.api.Location+xml">
  <id>133</id>
  <priority>3</priority>
  <hidden>true</hidden>
  <invisible>true</invisible>
  <ParentLocation href="/content/locations/1/5/73" media-type="application/vnd.ez.api.Location+xml"/>
  <pathString>/1/5/73/133</pathString>
  <depth>4</depth>
  <childCount>0</childCount>
  <remoteId>remoteId-qwert999</remoteId>
  <Children href="/content/locations/1/5/73/133/children" media-type="application/vnd.ez.api.LocationList+xml"/>
  <Content href="/content/objects/23" media-type="application/vnd.ez.api.Content+xml"/>
  <sortField>CLASS</sortField>
  <sortOrder>ASC</sortOrder>
</Location>
```

##### 401

Error - the user is not authorized to update this location

##### 404

Error - the Location with the given ID does not exist

### Swap Location

Swaps the content of the Location with the content of the given location. SWAP or POST with header X-HTTP-Method-Override SWAP

| Parameter                           | Value                               | 
| ----------------------------------- | ----------------------------------- | 
| URI                                 | `/content/locations/{locationId}`   | 
| Method                              | SWAP                                | 

#### Headers

##### Destination

A parent Location resource to which the Location is moved e.g. '/api/ezp/v2/content/locations/1/63'

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 204

No Content. Swapped the content of the Location with the content of the given location

##### 401

Error - the user is not authorized to swap this location

##### 404

Error - the Location with the given ID does not exist

### Create View

Executes a query and returns view including the results. The View input reflects the criteria model of the public API. Will respond with a 301, as the resource has been moved to /views (Platform 1.0) - DEPRECATED

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/content/views`   | 
| Method             | POST               | 

#### Headers

##### Accept

The view in XML or JSON format

| Parameter                                                                                                                                                                            | Value                                                                                                                                                                                | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | 
| Type                                                                                                                                                                                 | string                                                                                                                                                                               | 
| Default                                                                                                                                                                              | n/a                                                                                                                                                                                  | 
| Required                                                                                                                                                                             | no                                                                                                                                                                                   | 
| Example                                                                                                                                                                              | `application/vnd.ez.api.View+xml`<br>`application/vnd.ez.api.View+json`<br>`application/vnd.ez.api.View+xml; version=1.1`<br>`application/vnd.ez.api.View+json; version=1.1`<br>``   | 

##### Content-Type

The view input in XML or JSON format

| Parameter                                                                                                                                                                                                | Value                                                                                                                                                                                                    | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                                                     | string                                                                                                                                                                                                   | 
| Default                                                                                                                                                                                                  | n/a                                                                                                                                                                                                      | 
| Required                                                                                                                                                                                                 | no                                                                                                                                                                                                       | 
| Example                                                                                                                                                                                                  | `application/vnd.ez.api.ViewInput+xml`<br>`application/vnd.ez.api.ViewInput+json`<br>`application/vnd.ez.api.ViewInput+xml; version=1.1`<br>`application/vnd.ez.api.ViewInput+json; version=1.1`<br>``   | 

#### Responses

##### 301

Moved permanently

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

### List views

Returns a list of view URIs. The list includes public view and private view of the authenticated user. - DEPRECATED

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/content/views`   | 
| Method             | GET                | 

#### Headers

##### Accept

The view link list in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.RefList+xml`<br>`application/vnd.ez.api.RefList+json`<br>``   | 

#### Responses

##### 200

OK - list of view URIs

### Get View

Returns the view - DEPRECATED

| Parameter                       | Value                           | 
| ------------------------------- | ------------------------------- | 
| URI                             | `/content/views/{identifier}`   | 
| Method                          | GET                             | 

#### Headers

##### Accept

The view excluding results in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.View+xml`<br>`application/vnd.ez.api.View+json`<br>``   | 

#### Responses

##### 200

OK - returns the view

##### 401

Error - the view is not public and from another user

### Delete View

The given view is deleted - DEPRECATED

| Parameter                       | Value                           | 
| ------------------------------- | ------------------------------- | 
| URI                             | `/content/views/{identifier}`   | 
| Method                          | DELETE                          | 

#### Responses

##### 204

No content - the given view is deleted

##### 401

Error - the user is not authorized to delete this view

##### 404

Error - the view does not exist

### Get Results of existing View

Returns result of the view - DEPRECATED

| Parameter                               | Value                                   | 
| --------------------------------------- | --------------------------------------- | 
| URI                                     | `/content/views/{identifier}/results`   | 
| Method                                  | GET                                     | 

#### Headers

##### Accept

The view excluding results in XML or JSON format

| Parameter                                                                                   | Value                                                                                       | 
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | 
| Type                                                                                        | string                                                                                      | 
| Default                                                                                     | n/a                                                                                         | 
| Required                                                                                    | no                                                                                          | 
| Example                                                                                     | `application/vnd.ez.api.ViewResult+xml`<br>`application/vnd.ez.api.ViewResult+json`<br>``   | 

#### Responses

##### 200

OK - result of the view

##### 401

Error - the view is not public and from another user

### Create a new Section

Creates a new section

| Parameter             | Value                 | 
| --------------------- | --------------------- | 
| URI                   | `/content/sections`   | 
| Method                | POST                  | 

#### Headers

##### Accept

If set the new Section is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Section+xml`<br>`application/vnd.ez.api.Section+json`<br>``   | 

##### Content-Type

The Section input schema encoded in XML or JSON

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.SectionInput+json`<br>`application/vnd.ez.api.SectionInput+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.SectionInput+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | SectionInput   | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.Section+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Section     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/7">
    <sectionId>7</sectionId>
    <identifier>restricted</identifier>
    <name>Restricted</name>
</Section>
```

### Get Sections

Returns a list of all sections

| Parameter             | Value                 | 
| --------------------- | --------------------- | 
| URI                   | `/content/sections`   | 
| Method                | GET                   | 

#### Headers

##### Accept

If set the Section list is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.SectionList+xml`<br>`application/vnd.ez.api.SectionList+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Query Parameters

| Name                                                      | Type                                                      | Default                                                   | Required                                                  | Example                                                   | Description                                               | 
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | 
| identifer                                                 | string                                                    | n/a                                                       | no                                                        | n/a                                                       | Only the Section with the given identifier is returned.   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.SectionList+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | SectionList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SectionList media-type="application/vnd.ez.api.SectionList+xml" href="/api/ezp/v2/content/sections">
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1">
        <sectionId>1</sectionId>
        <identifier>standard</identifier>
        <name>Standard</name>
    </Section>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2">
        <sectionId>2</sectionId>
        <identifier>users</identifier>
        <name>Users</name>
    </Section>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/3">
        <sectionId>3</sectionId>
        <identifier>media</identifier>
        <name>Media</name>
    </Section>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/4">
        <sectionId>4</sectionId>
        <identifier>setup</identifier>
        <name>Setup</name>
    </Section>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/5">
        <sectionId>5</sectionId>
        <identifier>design</identifier>
        <name>Design</name>
    </Section>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/6">
        <sectionId>6</sectionId>
        <identifier>form</identifier>
        <name>Form</name>
    </Section>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/7">
        <sectionId>7</sectionId>
        <identifier>restricted</identifier>
        <name>Restricted</name>
    </Section>
</SectionList>
```

##### 401

Error - Iif the user has no permission to read the sections

### Get Section

Returns the Section given by Section ID

| Parameter                         | Value                             | 
| --------------------------------- | --------------------------------- | 
| URI                               | `/content/sections/{sectionId}`   | 
| Method                            | GET                               | 

#### Headers

##### Accept

If set the Section is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Section+xml`<br>`application/vnd.ez.api.Section+json`<br>``   | 

##### If-None-match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Section+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Section     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/5">
    <sectionId>5</sectionId>
    <identifier>design</identifier>
    <name>Design</name>
</Section>
```

##### 401

Error - the user is not authorized to read this section

##### 404

Error - the Section does not exist

### Update a Section

Updates a section. PATCH or POST with header X-HTTP-Method-Override PATCH

| Parameter                         | Value                             | 
| --------------------------------- | --------------------------------- | 
| URI                               | `/content/sections/{sectionId}`   | 
| Method                            | PATCH                             | 

#### Headers

##### Accept

If set the updated Section is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Section+xml`<br>`application/vnd.ez.api.Section+json`<br>``   | 

##### Content-Type

The Section input schema encoded in XML or JSON

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.SectionInput+xml`<br>`application/vnd.ez.api.SectionInput+json`<br>``   | 

##### If-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.SectionInput+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | SectionInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SectionInput>
  <identifier>template</identifier>
  <name>Template</name>
</SectionInput>
```

#### Responses

##### 200

OK - Section updated

###### Payload

##### application/vnd.ez.api.Section+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Section     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/7">
    <sectionId>7</sectionId>
    <identifier>template</identifier>
    <name>Template</name>
</Section>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to create this section

##### 403

Error - a Section with the given new identifier already exists

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

### Delete Section

The given Section is deleted

| Parameter                         | Value                             | 
| --------------------------------- | --------------------------------- | 
| URI                               | `/content/sections/{sectionId}`   | 
| Method                            | DELETE                            | 

#### Responses

##### 204

No Content - given Section is deleted

##### 401

Error - the user is not authorized to delete this section

##### 404

Error - the Section does not exist

### List Trash Items

Returns a list of all items in Trash

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/content/trash`   | 
| Method             | GET                | 

#### Headers

##### Accept

If set the Trash item list is returned in XML or JSON format

| Parameter                                                                         | Value                                                                             | 
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | 
| Type                                                                              | string                                                                            | 
| Default                                                                           | n/a                                                                               | 
| Required                                                                          | no                                                                                | 
| Example                                                                           | `application/vnd.ez.api.Trash+xml`<br>`application/vnd.ez.api.Trash+json`<br>``   | 

#### Query Parameters

| Name                                                           | Type                                                           | Default                                                        | Required                                                       | Example                                                        | Description                                                    | 
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | 
| limit                                                          | string                                                         | n/a                                                            | no                                                             | n/a                                                            | Only limit; items will be returned, starting with the offset   | 
| offset                                                         | string                                                         | n/a                                                            | no                                                             | n/a                                                            | Offset of the result set                                       | 

#### Responses

##### 200

OK - returns the list of items in Trash

###### Payload

##### application/vnd.ez.api.Trash+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Trash       | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Trash media-type="application/vnd.ez.api.Trash+xml" href="/api/ezp/v2/content/trash">
    <TrashItem media-type="application/vnd.ez.api.TrashItem+xml" href="/api/ezp/v2/content/trash/58">
        <id>58</id>
        <priority>0</priority>
        <hidden>false</hidden>
        <invisible>false</invisible>
        <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2/56"/>
        <pathString>/1/2/56/58/</pathString>
        <depth>3</depth>
        <childCount>0</childCount>
        <remoteId>59800915ad2eb8514de0bebe84f6ccba</remoteId>
        <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/52"/>
        <sortField>PATH</sortField>
        <sortOrder>ASC</sortOrder>
        <ContentInfo media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/52">
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/52" remoteId="881da87102313b0354dc2aa8f0e4b63b" id="52">
                <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/1"/>
                <Name>Folder 1</Name>
                <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/52/versions"/>
                <CurrentVersion media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/52/currentversion"/>
                <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/1"/>
                <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/52/locations"/>
                <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                <lastModificationDate>2019-02-06T09:03:09+01:00</lastModificationDate>
                <publishedDate>2019-02-06T09:03:09+01:00</publishedDate>
                <mainLanguageCode>eng-GB</mainLanguageCode>
                <currentVersionNo>1</currentVersionNo>
                <alwaysAvailable>true</alwaysAvailable>
                <ObjectStates media-type="application/vnd.ez.api.ContentObjectStates+xml" href="/api/ezp/v2/content/objects/52/objectstates"/>
            </Content>
        </ContentInfo>
    </TrashItem>
</Trash>
```

##### 401

Error - The user has no permission to read the trash

### Empty Trash

Empties the trash

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/content/trash`   | 
| Method             | DELETE             | 

#### Responses

##### 204

No Content - Trash emptied

##### 401

Error - The user is not authorized to empty all items from Trash

### Get TrashItem

Returns the item in Trash with the provided ID

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/trash/{trashItemid}`   | 
| Method                           | GET                              | 

#### Headers

##### Accept

If set the item in Trash is returned in XML or JSON format

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.TrashItem+xml`<br>`application/vnd.ez.api.TrashItem+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.TrashItem+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | TrashItem   | 

```xml
examples/content/trash/trash_itemid/GET/TrashItem.xml.example
```

##### 401

Error - The user has no permission to read the item in Trash

##### 404

Error - An item in Trash with the provided ID does not exist

### Untrash Item

Restores an item from Trash. MOVE or POST with header X-HTTP-Method-Override MOVE.

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/trash/{trashItemid}`   | 
| Method                           | MOVE                             | 

#### Headers

##### Destination

If the destination Location uri is provided, the item from Trash is restored under this Location, otherwise under its original parent Location

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 201

Item restored

##### 401

Error - The user is not authorized to restore this item from Trash

##### 403

Error - The provided parent Location does not exist

##### 404

Error - The provided item does not exist in Trash

### Delete TrashItem

Deletes the provided item from Trash

| Parameter                        | Value                            | 
| -------------------------------- | -------------------------------- | 
| URI                              | `/content/trash/{trashItemid}`   | 
| Method                           | DELETE                           | 

#### Responses

##### 204

No Content - item deleted

##### 401

Error - The user is not authorized to delete the provided item

##### 404

Error - The provided item does not exist in Trash

### List Global UrlAliases

Returns the list of global URL aliases

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/content/urlaliases`   | 
| Method                  | GET                     | 

#### Headers

##### Accept

If set the URL alias list contains only references and is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.UrlAliasRefList+xml`<br>`application/vnd.ez.api.UrlAliasRefList+json`<br>``   | 

#### Responses

##### 200

OK - returns the list of URL aliases

###### Payload

##### application/vnd.ez.api.UrlAliasRefList+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | UrlAliasRefList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?> <UrlAliasRefList media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/urlaliases"> <UrlAlias media-type="application/vnd.ez.api.UrlAlias+xml" href="/api/ezp/v2/content/urlaliases/0-2cecdff5f90b8595d76b68c417b09f36"/> </UrlAliasRefList>
```

##### 401

Error - The user has no permission to read URL aliases

### Create Url Alias

Creates a new URL alias

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/content/urlaliases`   | 
| Method                  | POST                    | 

#### Headers

##### Accept

If set the new URL alias is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.UrlAlias+xml`<br>`application/vnd.ez.api.UrlAlias+json`<br>``   | 

##### Content-Type

The URL alias input schema encoded in XML or JSON

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.UrlAliasCreate+xml`<br>`application/vnd.ez.api.UrlAliasCreate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.UrlAliasCreate+xml

| Parameter        | Value            | 
| ---------------- | ---------------- | 
| Type             | UrlAliasCreate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UrlAliasCreate type="LOCATION">
  <location href='/api/ezp/v2/content/locations/1/2/59' />
  <path>example-urlalias</path>
  <languageCode>eng-GB</languageCode>
  <alwaysAvailable>true</alwaysAvailable>
  <forward>true</forward>
</UrlAliasCreate>
```

#### Responses

##### 201

URL alias created

###### Payload

##### application/vnd.ez.api.UrlAlias+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UrlAlias    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UrlAlias media-type="application/vnd.ez.api.UrlAlias+xml" href="/api/ezp/v2/content/urlaliases/0-deca3dadca45c3dff7861274b8e67ed7" id="0-deca3dadca45c3dff7861274b8e67ed7" type="LOCATION">
    <location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/59"/>
    <path>/example-urlalias</path>
    <languageCodes>eng-GB</languageCodes>
    <alwaysAvailable>true</alwaysAvailable>
    <isHistory>false</isHistory>
    <forward>true</forward>
    <custom>true</custom>
</UrlAlias>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create a URL alias

##### 403

Error - A URL alias with the same identifier already exists

### Get UrlAlias

Returns the URL alias with the given ID

| Parameter                            | Value                                | 
| ------------------------------------ | ------------------------------------ | 
| URI                                  | `/content/urlaliases/{urlAliasId}`   | 
| Method                               | GET                                  | 

#### Headers

##### Accept

If set the URL alias is returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.UrlAlias+xml`<br>`application/vnd.ez.api.UrlAlias+json`<br>``   | 

#### Responses

##### 200

OK - returns the URL alias

###### Payload

##### application/vnd.ez.api.UrlAlias+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UrlAlias    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UrlAlias media-type="application/vnd.ez.api.UrlAlias+xml" href="/api/ezp/v2/content/urlaliases/0-2cecdff5f90b8595d76b68c417b09f36" id="0-2cecdff5f90b8595d76b68c417b09f36" type="RESOURCE">
    <resource>content/view/full</resource>
    <path>/example-global</path>
    <languageCodes>eng-GB</languageCodes>
    <alwaysAvailable>true</alwaysAvailable>
    <isHistory>false</isHistory>
    <forward>true</forward>
    <custom>true</custom>
</UrlAlias>
```

##### 401

Error - The user is not authorized to read URL aliases

##### 404

Error - The URL alias does not exist

### Delete UrlAlias

Deleted the provided URL alias

| Parameter                            | Value                                | 
| ------------------------------------ | ------------------------------------ | 
| URI                                  | `/content/urlaliases/{urlAliasId}`   | 
| Method                               | DELETE                               | 

#### Responses

##### 204

No Content - URL alias deleted

##### 401

Error - The user is not authorized to delete a URL alias

##### 404

Error - The URL alias does not exist

### List Url Wildcards

Returns a list of URL wildcards

| Parameter                 | Value                     | 
| ------------------------- | ------------------------- | 
| URI                       | `/content/urlwildcards`   | 
| Method                    | GET                       | 

#### Headers

##### Accept

If set the URL wildcard is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.UrlWildcardList+xml`<br>`application/vnd.ez.api.UrlWildcardList+json`<br>``   | 

#### Responses

##### 200

OK - returns a list of URL wildcards

###### Payload

##### application/vnd.ez.api.UrlWildcardList+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | UrlWildcardList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UrlWildcardList media-type="application/vnd.ez.api.UrlWildcardList+xml" href="/api/ezp/v2/content/urlwildcards">
    <UrlWildcard media-type="application/vnd.ez.api.UrlWildcard+xml" href="/api/ezp/v2/content/urlwildcards/1" id="1">
        <sourceUrl>/api/ezp/v2/content/location/2</sourceUrl>
        <destinationUrl>/api/ezp/v2/content/location/59</destinationUrl>
        <forward>true</forward>
    </UrlWildcard>
</UrlWildcardList>
```

##### 401

Error - The user has no permission to read URL wildcards

### Create Url Wildcard

Creates a new URL wildcard

| Parameter                 | Value                     | 
| ------------------------- | ------------------------- | 
| URI                       | `/content/urlwildcards`   | 
| Method                    | POST                      | 

#### Headers

##### Accept

If set the new URL wildcard is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.UrlWildcard+xml`<br>`application/vnd.ez.api.UrlWildcard+json`<br>``   | 

##### Content-Type

The URL Wildcard input schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.UrlWildcardCreate+xml`<br>`application/vnd.ez.api.UrlWildcardCreate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.UrlWildcardCreate.xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | UrlWildcardCreate   | 

#### Responses

##### 201

URL wildcard created

###### Payload

##### application/vnd.ez.api.UrlWildcard+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | UrlWildcard   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UrlWildcard media-type="application/vnd.ez.api.UrlWildcard+xml" href="/api/ezp/v2/content/urlwildcards/1" id="1">
    <sourceUrl>/api/ezp/v2/content/location/2</sourceUrl>
    <destinationUrl>/api/ezp/v2/content/location/59</destinationUrl>
    <forward>true</forward>
</UrlWildcard>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create a URL wildcard

##### 403

Error - A URL wildcard with the same identifier already exists

### Get Url Wildcard

Returns the URL wildcard with the given ID

| Parameter                              | Value                                  | 
| -------------------------------------- | -------------------------------------- | 
| URI                                    | `/content/urlwildcards/{wildcardId}`   | 
| Method                                 | GET                                    | 

#### Headers

##### Accept

If set the URL wildcard is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.UrlWildcard+xml`<br>`application/vnd.ez.api.UrlWildcard+json`<br>``   | 

#### Responses

##### 200

OK - returns the URL wildcard

###### Payload

##### application/vnd.ez.api.UrlWildcard+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | UrlWildcard   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UrlWildcard media-type="application/vnd.ez.api.UrlWildcard+xml" href="/api/ezp/v2/content/urlwildcards/1" id="1">
    <sourceUrl>/api/ezp/v2/content/location/2</sourceUrl>
    <destinationUrl>/api/ezp/v2/content/location/59</destinationUrl>
    <forward>true</forward>
</UrlWildcard>
```

##### 401

Error - The user is not authorized to read URL wildcards

##### 404

Error - The URL wildcard does not exist

### Delete Url Wildcard

Deletes the given URL wildcard

| Parameter                              | Value                                  | 
| -------------------------------------- | -------------------------------------- | 
| URI                                    | `/content/urlwildcards/{wildcardId}`   | 
| Method                                 | DELETE                                 | 

#### Responses

##### 204

No Content - URL wildcard deleted

##### 401

Error - The user is not authorized to delete a URL wildcard

##### 404

Error - The URL wildcard does not exist

### Get Content Type Groups

Returns a list of all Content Type Groups. If an identifier is provided, loads the Content Type Group for this identifier

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/content/typegroups`   | 
| Method                  | GET                     | 

#### Headers

##### Accept

If set the Content Type Group list is returned in XML or JSON format

| Parameter                                                                                                       | Value                                                                                                           | 
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                            | string                                                                                                          | 
| Default                                                                                                         | n/a                                                                                                             | 
| Required                                                                                                        | no                                                                                                              | 
| Example                                                                                                         | `application/vnd.ez.api.ContentTypeGroupList+xml`<br>`application/vnd.ez.api.ContentTypeGroupList+json`<br>``   | 

#### Query Parameters

| Name                                                                                                             | Type                                                                                                             | Default                                                                                                          | Required                                                                                                         | Example                                                                                                          | Description                                                                                                      | 
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | 
| identifier                                                                                                       | string                                                                                                           | n/a                                                                                                              | no                                                                                                               | n/a                                                                                                              | The identifier of the Content Type Group. If present, the Content Type Group with this identifier is returned.   | 

#### Responses

##### 200

OK - returns a list of Content Type Groups

###### Payload

##### application/vnd.ez.api.ContentTypeGroupList+xml

| Parameter              | Value                  | 
| ---------------------- | ---------------------- | 
| Type                   | ContentTypeGroupList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroupList media-type="application/vnd.ez.api.ContentTypeGroupList+xml" href="/api/ezp/v2/content/typegroups">
    <ContentTypeGroup media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/1">
        <id>1</id>
        <identifier>Content</identifier>
        <created>2002-09-05T11:08:48+02:00</created>
        <modified>2002-10-06T18:35:06+02:00</modified>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <ContentTypes media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/typegroups/1/types"/>
    </ContentTypeGroup>
    <ContentTypeGroup media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/2">
        <id>2</id>
        <identifier>Users</identifier>
        <created>2002-09-05T11:09:01+02:00</created>
        <modified>2002-10-06T18:35:13+02:00</modified>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <ContentTypes media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/typegroups/2/types"/>
    </ContentTypeGroup>
    <ContentTypeGroup media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/3">
        <id>3</id>
        <identifier>Media</identifier>
        <created>2002-09-14T15:22:23+02:00</created>
        <modified>2002-10-06T18:35:20+02:00</modified>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <ContentTypes media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/typegroups/3/types"/>
    </ContentTypeGroup>
</ContentTypeGroupList>
```

##### 307

Temporary Redirect

##### 401

Error - The user has no permission to read Content Types

##### 404

Error - The Content Type Group with the given identifier does not exist

### Create Content Type Group

Creates a new Content Type Group

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/content/typegroups`   | 
| Method                  | POST                    | 

#### Headers

##### Accept

If set the new Content Type Group is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.ContentTypeGroup+xml`<br>`application/vnd.ez.api.ContentTypeGroup+json`<br>``   | 

##### Content-Type

The Content Type Group input schema encoded in XML or JSON

| Parameter                                                                                                         | Value                                                                                                             | 
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                              | string                                                                                                            | 
| Default                                                                                                           | n/a                                                                                                               | 
| Required                                                                                                          | no                                                                                                                | 
| Example                                                                                                           | `application/vnd.ez.api.ContentTypeGroupInput+xml`<br>`application/vnd.ez.api.ContentTypeGroupInput+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.ContentTypeGroupInput+xml

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| Type                    | ContentTypeGroupInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroupInput>
    <identifier>newContentTypeGroup</identifier>
</ContentTypeGroupInput>
```

#### Responses

##### 201

Content Type Group created

###### Payload

##### application/vnd.ez.api.ContentTypeGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ContentTypeGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroup href="/content/typesgroups/7" media-type="application/vnd.ez.api.ContentTypeGroup+xml">
    <id>7</id>
    <identifier>newContentTypeGroup</identifier>
    <created>2012-02-31T12:45:00</created>
    <modified>2012-02-31T12:45:00</modified>
    <Creator href="/user/users/13" media-type="application/vnd.ez.api.User+xml"/>
    <Modifier href="/user/users/13" media-type="application/vnd.ez.api.User+xml"/>
    <ContentTypes href="/content/typegroups/7/types" media-type="application/vnd.ez.api.ContentTypeList+xml"/>
</ContentTypeGroup>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create this Content Type Group

##### 403

Error - A Content Type Group with the same identifier already exists

### Get Content Type Group

Returns the Content Type Group with the provided ID

| Parameter                                    | Value                                        | 
| -------------------------------------------- | -------------------------------------------- | 
| URI                                          | `/content/typegroups/{contentTypeGroupId}`   | 
| Method                                       | GET                                          | 

#### Headers

##### Accept

If set the Content Type Group is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.ContentTypeGroup+xml`<br>`application/vnd.ez.api.ContentTypeGroup+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns the Content Type Group

###### Payload

##### application/vnd.ez.api.ContentTypeGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ContentTypeGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroup media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/1">
    <id>1</id>
    <identifier>Content</identifier>
    <created>2002-09-05T11:08:48+02:00</created>
    <modified>2002-10-06T18:35:06+02:00</modified>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <ContentTypes media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/typegroups/1/types"/>
</ContentTypeGroup>
```

##### 401

Error - The user is not authorized to read this Content Type Group

##### 404

Error - The Content Type Group does not exist

### Update Content Type Group

Updates a Content Type Group. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                                    | Value                                        | 
| -------------------------------------------- | -------------------------------------------- | 
| URI                                          | `/content/typegroups/{contentTypeGroupId}`   | 
| Method                                       | PATCH                                        | 

#### Headers

##### Accept

If set the updated Content Type Group is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.ContentTypeGroup+xml`<br>`application/vnd.ez.api.ContentTypeGroup+json`<br>``   | 

##### Content-Type

The Content Type Group input schema encoded in XML or JSON

| Parameter                                                                                                         | Value                                                                                                             | 
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                              | string                                                                                                            | 
| Default                                                                                                           | n/a                                                                                                               | 
| Required                                                                                                          | no                                                                                                                | 
| Example                                                                                                           | `application/vnd.ez.api.ContentTypeGroupInput+xml`<br>`application/vnd.ez.api.ContentTypeGroupInput+json`<br>``   | 

##### If-Match

ETag causes patching only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.ContentTypeGroupInput+xml

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| Type                    | ContentTypeGroupInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroupInput>
    <identifier>updatedIdentifer</identifier>
</ContentTypeGroupInput>
```

#### Responses

##### 200

Content Type Group updated

###### Payload

##### application/vnd.ez.api.ContentTypeGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ContentTypeGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroup media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/1">
    <id>4</id>
    <identifier>updatedIdentifer</identifier>
    <created>2002-09-05T11:08:48+02:00</created>
    <modified>2019-02-22T14:42:55+01:00</modified>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <ContentTypes media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/typegroups/1/types"/>
</ContentTypeGroup>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create this Content Type group

##### 403

Error - A Content Type Group with the given identifier already exists

##### 412

Error - The current ETag does not match the one provided in the If-Match header

### Delete Content Type Group

Deletes the provided Content Type Group

| Parameter                                    | Value                                        | 
| -------------------------------------------- | -------------------------------------------- | 
| URI                                          | `/content/typegroups/{contentTypeGroupId}`   | 
| Method                                       | DELETE                                       | 

#### Responses

##### 204

No Content - Content Type Group deleted

##### 401

Error - The user is not authorized to delete this Content Type Group

##### 403

Error - The Content Type Group is not empty

##### 404

Error - The Content Type Group does not exist

### List Content Types for Group

Returns a list of Content Types in the provided group

| Parameter                                          | Value                                              | 
| -------------------------------------------------- | -------------------------------------------------- | 
| URI                                                | `/content/typegroups/{contentTypeGroupId}/types`   | 
| Method                                             | GET                                                | 

#### Headers

##### Accept

If set the list of Content Type info objects or Content Types (including Field definitions) is returned in XML or JSON format

| Parameter                                                                                                                                                                                                      | Value                                                                                                                                                                                                          | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                                                           | string                                                                                                                                                                                                         | 
| Default                                                                                                                                                                                                        | n/a                                                                                                                                                                                                            | 
| Required                                                                                                                                                                                                       | no                                                                                                                                                                                                             | 
| Example                                                                                                                                                                                                        | `application/vnd.ez.api.ContentTypeInfoList+xml`<br>`application/vnd.ez.api.ContentTypeInfoList+json`<br>`application/vnd.ez.api.ContentTypeList+xml`<br>`application/vnd.ez.api.ContentTypeList+json`<br>``   | 

#### Responses

##### 200

OK - returns a list on Content Types

###### Payload

##### application/vnd.ez.api.ContentTypeInfoList+xml

| Parameter             | Value                 | 
| --------------------- | --------------------- | 
| Type                  | ContentTypeInfoList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeInfoList media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/typegroups/1/types">
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/2">
        <id>2</id>
        <status>DEFINED</status>
        <identifier>article</identifier>
        <names>
            <value languageCode="eng-GB">Article</value>
        </names>
        <descriptions/>
        <creationDate>2002-06-18T11:21:38+02:00</creationDate>
        <modificationDate>2004-04-20T11:56:29+02:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/2/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2/draft"/>
        <remoteId>c15b600eb9198b1924063b5a68758232</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_title|title&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/1">
        <id>1</id>
        <status>DEFINED</status>
        <identifier>folder</identifier>
        <names>
            <value languageCode="eng-GB">Folder</value>
        </names>
        <descriptions/>
        <creationDate>2002-06-18T11:21:38+02:00</creationDate>
        <modificationDate>2015-11-29T22:14:32+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/1/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/1/draft"/>
        <remoteId>a3d405b81be900468eb153d774f4f0d2</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_name|name&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>
</ContentTypeInfoList>
```

##### application/vnd.ez.api.ContentTypeList+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | ContentTypeList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeList media-type="application/vnd.ez.api.ContentTypeList+xml" href="/api/ezp/v2/content/typegroups/1/types">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2">
        <id>2</id>
        <status>DEFINED</status>
        <identifier>article</identifier>
        <names>
            <value languageCode="eng-GB">Article</value>
        </names>
        <descriptions/>
        <creationDate>2002-06-18T11:21:38+02:00</creationDate>
        <modificationDate>2004-04-20T11:56:29+02:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/2/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2/draft"/>
        <remoteId>c15b600eb9198b1924063b5a68758232</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_title|title&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
        <FieldDefinitions media-type="application/vnd.ez.api.FieldDefinitionList+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions">
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/1">
                <id>1</id>
                <identifier>title</identifier>
                <fieldType>ezstring</fieldType>
                <fieldGroup></fieldGroup>
                <position>1</position>
                <isTranslatable>true</isTranslatable>
                <isRequired>true</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue>New article</defaultValue>
                <isSearchable>true</isSearchable>
                <names>
                    <value languageCode="eng-GB">Title</value>
                </names>
                <descriptions/>
                <fieldSettings/>
                <validatorConfiguration>
                    <value key="StringLengthValidator">
                        <value key="maxStringLength">255</value>
                        <value key="minStringLength"/></value>
                </validatorConfiguration>
            </FieldDefinition>
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/152">
                <id>152</id>
                <identifier>short_title</identifier>
                <fieldType>ezstring</fieldType>
                <fieldGroup></fieldGroup>
                <position>2</position>
                <isTranslatable>true</isTranslatable>
                <isRequired>false</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue/>
                <isSearchable>true</isSearchable>
                <names>
                    <value languageCode="eng-GB">Short title</value>
                </names>
                <descriptions/>
                <fieldSettings/>
                <validatorConfiguration>
                    <value key="StringLengthValidator">
                        <value key="maxStringLength">255</value>
                        <value key="minStringLength"/></value>
                </validatorConfiguration>
            </FieldDefinition>
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/153">
                <id>153</id>
                <identifier>author</identifier>
                <fieldType>ezauthor</fieldType>
                <fieldGroup></fieldGroup>
                <position>3</position>
                <isTranslatable>true</isTranslatable>
                <isRequired>false</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue/>
                <isSearchable>false</isSearchable>
                <names>
                    <value languageCode="eng-GB">Author</value>
                </names>
                <descriptions/>
                <fieldSettings>
                    <value key="defaultAuthor">1</value>
                </fieldSettings>
                <validatorConfiguration/>
            </FieldDefinition>
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/120">
                <id>120</id>
                <identifier>intro</identifier>
                <fieldType>ezrichtext</fieldType>
                <fieldGroup></fieldGroup>
                <position>4</position>
                <isTranslatable>true</isTranslatable>
                <isRequired>true</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue>
                    <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; version=&quot;5.0-variant ezpublish-1.0&quot;/&gt;
</value>
                    <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;/&gt;
</value>
                </defaultValue>
                <isSearchable>true</isSearchable>
                <names>
                    <value languageCode="eng-GB">Intro</value>
                </names>
                <descriptions/>
                <fieldSettings/>
                <validatorConfiguration/>
            </FieldDefinition>
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/121">
                <id>121</id>
                <identifier>body</identifier>
                <fieldType>ezrichtext</fieldType>
                <fieldGroup></fieldGroup>
                <position>5</position>
                <isTranslatable>true</isTranslatable>
                <isRequired>false</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue>
                    <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; version=&quot;5.0-variant ezpublish-1.0&quot;/&gt;
</value>
                    <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;/&gt;
</value>
                </defaultValue>
                <isSearchable>true</isSearchable>
                <names>
                    <value languageCode="eng-GB">Body</value>
                </names>
                <descriptions/>
                <fieldSettings/>
                <validatorConfiguration/>
            </FieldDefinition>
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/123">
                <id>123</id>
                <identifier>enable_comments</identifier>
                <fieldType>ezboolean</fieldType>
                <fieldGroup></fieldGroup>
                <position>6</position>
                <isTranslatable>false</isTranslatable>
                <isRequired>false</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue>false</defaultValue>
                <isSearchable>false</isSearchable>
                <names>
                    <value languageCode="eng-GB">Enable comments</value>
                </names>
                <descriptions/>
                <fieldSettings/>
                <validatorConfiguration/>
            </FieldDefinition>
            <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/154">
                <id>154</id>
                <identifier>image</identifier>
                <fieldType>ezobjectrelation</fieldType>
                <fieldGroup></fieldGroup>
                <position>7</position>
                <isTranslatable>true</isTranslatable>
                <isRequired>false</isRequired>
                <isInfoCollector>false</isInfoCollector>
                <defaultValue>
                    <value key="destinationContentId"/>
                </defaultValue>
                <isSearchable>true</isSearchable>
                <names>
                    <value languageCode="eng-GB">Image</value>
                </names>
                <descriptions/>
                <fieldSettings>
                    <value key="selectionMethod">SELECTION_BROWSE</value>
                    <value key="selectionRoot"></value>
                    <value key="selectionContentTypes"/>
                </fieldSettings>
                <validatorConfiguration/>
            </FieldDefinition>
        </FieldDefinitions>
    </ContentType>
</ContentTypeList>
```

##### 401

Error - The user has no permission to read the Content Types

### Create Content Type

Creates a new Content Type draft in the given Content Type Group

| Parameter                                          | Value                                              | 
| -------------------------------------------------- | -------------------------------------------------- | 
| URI                                                | `/content/typegroups/{contentTypeGroupId}/types`   | 
| Method                                             | POST                                               | 

#### Headers

##### Accept

If set the new Content Type or draft is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.ContentType+xml`<br>`application/vnd.ez.api.ContentType+json`<br>``   | 

##### Content-Type

The Content Type Create schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.ContentTypeCreate+xml`<br>`application/vnd.ez.api.ContentTypeCreate+json`<br>``   | 

#### Query Parameters

| Name                                                                    | Type                                                                    | Default                                                                 | Required                                                                | Example                                                                 | Description                                                             | 
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | 
| publish                                                                 | boolean                                                                 | n/a                                                                     | no                                                                      | n/a                                                                     | If true, the Content Type is published after creating (default false)   | 

#### Payload

##### application/vnd.ez.api.ContentTypeCreate.xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | ContentTypeCreate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeCreate>
  <identifier>newContentType</identifier>
  <names>
    <value languageCode="eng-US">New Content Type</value>
  </names>
  <descriptions>
    <value languageCode="eng-US">This is a description</value>
  </descriptions>
  <remoteId>remoteId-qwert548</remoteId>
  <urlAliasSchema>&lt;title&gt;</urlAliasSchema>
  <nameSchema>&lt;title&gt;</nameSchema>
  <isContainer>true</isContainer>
  <mainLanguageCode>eng-US</mainLanguageCode>
  <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
  <defaultSortField>PATH</defaultSortField>
  <defaultSortOrder>ASC</defaultSortOrder>
  <FieldDefinitions>
    <FieldDefinition>
      <identifier>title</identifier>
      <fieldType>ezstring</fieldType>
      <fieldGroup>content</fieldGroup>
      <position>1</position>
      <isTranslatable>true</isTranslatable>
      <isRequired>true</isRequired>
      <isInfoCollector>false</isInfoCollector>
      <defaultValue>New Title</defaultValue>
      <isSearchable>true</isSearchable>
      <names>
        <value languageCode="eng-US">Title</value>
      </names>
      <descriptions>
        <value languageCode="eng-US">This is the title</value>
      </descriptions>
    </FieldDefinition>
    <FieldDefinition>
      <identifier>summary</identifier>
      <fieldType>ezxmltext</fieldType>
      <fieldGroup>content</fieldGroup>
      <position>2</position>
      <isTranslatable>true</isTranslatable>
      <isRequired>false</isRequired>
      <isInfoCollector>false</isInfoCollector>
      <defaultValue>
        <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&lt;section/&gt;</value>
      </defaultValue>
      <isSearchable>true</isSearchable>
      <names>
        <value languageCode="eng-US">Summary</value>
      </names>
      <descriptions>
        <value languageCode="eng-US">This is the summary</value>
      </descriptions>
    </FieldDefinition>
   </FieldDefinitions>
</ContentTypeCreate>
```

#### Responses

##### 201

Content Type created

###### Payload

##### application/vnd.ez.api.ContentType+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentType   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/20/draft">
    <id>20</id>
    <status>DRAFT</status>
    <identifier>newContentType</identifier>
    <names>
        <value languageCode="eng-GB">New Content Type</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">This is a description</value>
    </descriptions>
    <creationDate>2019-02-26T09:39:58+01:00</creationDate>
    <modificationDate>2019-02-26T09:39:58+01:00</modificationDate>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/20/groups"/>
    <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/20/draft"/>
    <remoteId>remoteId-qwert548</remoteId>
    <urlAliasSchema>&lt;title&gt;</urlAliasSchema>
    <nameSchema>&lt;title&gt;</nameSchema>
    <isContainer>true</isContainer>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
    <defaultSortField>PATH</defaultSortField>
    <defaultSortOrder>ASC</defaultSortOrder>
    <FieldDefinitions media-type="application/vnd.ez.api.FieldDefinitionList+xml" href="/api/ezp/v2/content/types/20/draft/fieldDefinitions">
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/20/draft/fieldDefinitions/223">
            <id>223</id>
            <identifier>title</identifier>
            <fieldType>ezstring</fieldType>
            <fieldGroup>content</fieldGroup>
            <position>1</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>true</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>New Title</defaultValue>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Title</value>
            </names>
            <descriptions>
                <value languageCode="eng-GB">This is the title</value>
            </descriptions>
            <fieldSettings/>
            <validatorConfiguration>
                <value key="StringLengthValidator">
                    <value key="minStringLength">0</value>
                    <value key="maxStringLength"/></value>
            </validatorConfiguration>
        </FieldDefinition>
    </FieldDefinitions>
</ContentType>
```

##### 400

Error - The input does not match the input schema definition. Validation on a field definition fails. Validation of the Content Type fails, e.g. multiple Fields of a same singular Field Type are provided. publish is set to true and the input is not complete e.g. no field definitions are provided.

##### 401

Error - The user is not authorized to create this Content Type

##### 403

Error - A Content Type with same identifier already exists

### List Content Types

Returns a list of Content Types

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/content/types`   | 
| Method             | GET                | 

#### Headers

##### Accept

If set the list of Content Type info objects or Content Types (including Field definitions) is returned in XML or JSON format

| Parameter                                                                                                                                                                                                      | Value                                                                                                                                                                                                          | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                                                           | string                                                                                                                                                                                                         | 
| Default                                                                                                                                                                                                        | n/a                                                                                                                                                                                                            | 
| Required                                                                                                                                                                                                       | no                                                                                                                                                                                                             | 
| Example                                                                                                                                                                                                        | `application/vnd.ez.api.ContentTypeInfoList+xml`<br>`application/vnd.ez.api.ContentTypeInfoList+json`<br>`application/vnd.ez.api.ContentTypeList+xml`<br>`application/vnd.ez.api.ContentTypeList+json`<br>``   | 

#### Query Parameters

| Name                                                                  | Type                                                                  | Default                                                               | Required                                                              | Example                                                               | Description                                                           | 
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | 
| identifier                                                            | string                                                                | n/a                                                                   | no                                                                    | n/a                                                                   | Retrieves the Content Type for the given identifer                    | 
| remoteId                                                              | string                                                                | n/a                                                                   | no                                                                    | n/a                                                                   | Retrieves the Content Type for the given remoteId                     | 
| limit                                                                 | string                                                                | n/a                                                                   | no                                                                    | n/a                                                                   | Only &lt;limit&gt; items will be returned, starting with the offset   | 
| offset                                                                | string                                                                | n/a                                                                   | no                                                                    | n/a                                                                   | Offset of the result set                                              | 
| orderby                                                               | string                                                                | n/a                                                                   | no                                                                    | n/a                                                                   | One of (name|lastmodified)                                            | 
| sort                                                                  | string                                                                | n/a                                                                   | no                                                                    | n/a                                                                   | One of (asc|desc)                                                     | 

#### Responses

##### 200

OK - returns a list of Content Types

###### Payload

##### application/vnd.ez.api.ContentTypeInfoList+xml

| Parameter             | Value                 | 
| --------------------- | --------------------- | 
| Type                  | ContentTypeInfoList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeInfoList media-type="application/vnd.ez.api.ContentTypeInfoList+xml" href="/api/ezp/v2/content/types">
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/2">
        <id>2</id>
        <status>DEFINED</status>
        <identifier>article</identifier>
        <names>
            <value languageCode="eng-GB">Article</value>
        </names>
        <descriptions/>
        <creationDate>2002-06-18T11:21:38+02:00</creationDate>
        <modificationDate>2004-04-20T11:56:29+02:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/2/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2/draft"/>
        <remoteId>c15b600eb9198b1924063b5a68758232</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_title|title&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/13">
        <id>13</id>
        <status>DEFINED</status>
        <identifier>copy_of_article_13</identifier>
        <names>
            <value languageCode="eng-GB">Article</value>
        </names>
        <descriptions/>
        <creationDate>2019-02-06T10:55:12+01:00</creationDate>
        <modificationDate>2019-02-06T10:55:12+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/13/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/13/draft"/>
        <remoteId>b045340aaa8a7a1111f5a6bed6e70715</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_title|title&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/14">
        <id>14</id>
        <status>DEFINED</status>
        <identifier>copy_of_article_14</identifier>
        <names>
            <value languageCode="eng-GB">Article</value>
        </names>
        <descriptions/>
        <creationDate>2019-02-06T10:56:36+01:00</creationDate>
        <modificationDate>2019-02-06T10:56:36+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/14/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/14/draft"/>
        <remoteId>d7ae816f22fe929e67a359a2ef6e7cde</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_title|title&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/1">
        <id>1</id>
        <status>DEFINED</status>
        <identifier>folder</identifier>
        <names>
            <value languageCode="eng-GB">Folder</value>
        </names>
        <descriptions/>
        <creationDate>2002-06-18T11:21:38+02:00</creationDate>
        <modificationDate>2015-11-29T22:14:32+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/1/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/1/draft"/>
        <remoteId>a3d405b81be900468eb153d774f4f0d2</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;short_name|name&gt;</nameSchema>
        <isContainer>true</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>
    <ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/4">
        <id>4</id>
        <status>DEFINED</status>
        <identifier>user</identifier>
        <names>
            <value languageCode="eng-GB">User</value>
        </names>
        <descriptions/>
        <creationDate>2002-06-18T11:21:38+02:00</creationDate>
        <modificationDate>2004-04-15T10:39:24+02:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/4/groups"/>
        <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/4/draft"/>
        <remoteId>40faa822edc579b02c25f6bb7beec3ad</remoteId>
        <urlAliasSchema></urlAliasSchema>
        <nameSchema>&lt;first_name&gt; &lt;last_name&gt;</nameSchema>
        <isContainer>false</isContainer>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
        <defaultSortField>PATH</defaultSortField>
        <defaultSortOrder>ASC</defaultSortOrder>
    </ContentTypeInfo>

</ContentTypeInfoList>
```

##### 401

Error - The user has no permission to read the Content Types

### Get Content Type

Returns the Content Type with the provided ID

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/content/types/{contentTypeId}`   | 
| Method                             | GET                                | 

#### Headers

##### Accept

If set the Content Type is returned in XML or JSON format

| Parameter                                                                                     | Value                                                                                         | 
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | 
| Type                                                                                          | string                                                                                        | 
| Default                                                                                       | n/a                                                                                           | 
| Required                                                                                      | no                                                                                            | 
| Example                                                                                       | `application/vnd.ez.api.ContentType+xml`<br>`application/vnd.ez.api.ContentType+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - returns the Content Type

###### Payload

##### application/vnd.ez.api.ContentType+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentType   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2">
    <id>2</id>
    <status>DEFINED</status>
    <identifier>article</identifier>
    <names>
        <value languageCode="eng-GB">Article</value>
    </names>
    <descriptions/>
    <creationDate>2002-06-18T11:21:38+02:00</creationDate>
    <modificationDate>2004-04-20T11:56:29+02:00</modificationDate>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/2/groups"/>
    <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/2/draft"/>
    <remoteId>c15b600eb9198b1924063b5a68758232</remoteId>
    <urlAliasSchema></urlAliasSchema>
    <nameSchema>&lt;short_title|title&gt;</nameSchema>
    <isContainer>true</isContainer>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
    <defaultSortField>PATH</defaultSortField>
    <defaultSortOrder>ASC</defaultSortOrder>
    <FieldDefinitions media-type="application/vnd.ez.api.FieldDefinitionList+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions">
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/1">
            <id>1</id>
            <identifier>title</identifier>
            <fieldType>ezstring</fieldType>
            <fieldGroup></fieldGroup>
            <position>1</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>true</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>New article</defaultValue>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Title</value>
            </names>
            <descriptions/>
            <fieldSettings/>
            <validatorConfiguration>
                <value key="StringLengthValidator">
                    <value key="maxStringLength">255</value>
                    <value key="minStringLength"/></value>
            </validatorConfiguration>
        </FieldDefinition>
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/152">
            <id>152</id>
            <identifier>short_title</identifier>
            <fieldType>ezstring</fieldType>
            <fieldGroup></fieldGroup>
            <position>2</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>false</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue/>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Short title</value>
            </names>
            <descriptions/>
            <fieldSettings/>
            <validatorConfiguration>
                <value key="StringLengthValidator">
                    <value key="maxStringLength">255</value>
                    <value key="minStringLength"/></value>
            </validatorConfiguration>
        </FieldDefinition>
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/153">
            <id>153</id>
            <identifier>author</identifier>
            <fieldType>ezauthor</fieldType>
            <fieldGroup></fieldGroup>
            <position>3</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>false</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue/>
            <isSearchable>false</isSearchable>
            <names>
                <value languageCode="eng-GB">Author</value>
            </names>
            <descriptions/>
            <fieldSettings>
                <value key="defaultAuthor">1</value>
            </fieldSettings>
            <validatorConfiguration/>
        </FieldDefinition>
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/120">
            <id>120</id>
            <identifier>intro</identifier>
            <fieldType>ezrichtext</fieldType>
            <fieldGroup></fieldGroup>
            <position>4</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>true</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; version=&quot;5.0-variant ezpublish-1.0&quot;/&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;/&gt;
</value>
            </defaultValue>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Intro</value>
            </names>
            <descriptions/>
            <fieldSettings/>
            <validatorConfiguration/>
        </FieldDefinition>
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/121">
            <id>121</id>
            <identifier>body</identifier>
            <fieldType>ezrichtext</fieldType>
            <fieldGroup></fieldGroup>
            <position>5</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>false</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>
                <value key="xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://docbook.org/ns/docbook&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot; version=&quot;5.0-variant ezpublish-1.0&quot;/&gt;
</value>
                <value key="xhtml5edit">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;section xmlns=&quot;http://ez.no/namespaces/ezpublish5/xhtml5/edit&quot;/&gt;
</value>
            </defaultValue>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Body</value>
            </names>
            <descriptions/>
            <fieldSettings/>
            <validatorConfiguration/>
        </FieldDefinition>
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/123">
            <id>123</id>
            <identifier>enable_comments</identifier>
            <fieldType>ezboolean</fieldType>
            <fieldGroup></fieldGroup>
            <position>6</position>
            <isTranslatable>false</isTranslatable>
            <isRequired>false</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>false</defaultValue>
            <isSearchable>false</isSearchable>
            <names>
                <value languageCode="eng-GB">Enable comments</value>
            </names>
            <descriptions/>
            <fieldSettings/>
            <validatorConfiguration/>
        </FieldDefinition>
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/2/fieldDefinitions/154">
            <id>154</id>
            <identifier>image</identifier>
            <fieldType>ezobjectrelation</fieldType>
            <fieldGroup></fieldGroup>
            <position>7</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>false</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>
                <value key="destinationContentId"/>
            </defaultValue>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Image</value>
            </names>
            <descriptions/>
            <fieldSettings>
                <value key="selectionMethod">SELECTION_BROWSE</value>
                <value key="selectionRoot"></value>
                <value key="selectionContentTypes"/>
            </fieldSettings>
            <validatorConfiguration/>
        </FieldDefinition>
    </FieldDefinitions>
</ContentType>
```

##### 401

Error - The user is not authorized to read this Content Type

##### 404

Error - The Content Type does not exist

### Copy Content Type

Copies a Content Type. A new remoteId is generated, and the identifier of the copy is set to copy_of_%lt;originalBaseIdentifier&gt;_&lt;newTypeId&gt; (or another random string). COPY or POST with header X-HTTP-Method-Override COPY.

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/content/types/{contentTypeId}`   | 
| Method                             | COPY                               | 

#### Responses

##### 201

Copy of the Content Type created

##### 401

Error - The user is not authorized to copy this Content Type

### Create Draft

Creates a draft and updates it with the given data

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/content/types/{contentTypeId}`   | 
| Method                             | POST                               | 

#### Headers

##### Accept

If set the new Content Type draft is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.ContentTypeInfo+xml`<br>`application/vnd.ez.api.ContentTypeInfo+json`<br>``   | 

##### Content-Type

The Content Type Update schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.ContentTypeUpdate+xml`<br>`application/vnd.ez.api.ContentTypeUpdate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.ContentTypeUpdate+xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | ContentTypeUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeUpdate>
    <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
</ContentTypeUpdate>
```

#### Responses

##### 201

Draft created

###### Payload

##### application/vnd.ez.api.ContentTypeInfo+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | ContentTypeInfo   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/3/draft">
    <id>3</id>
    <status>DRAFT</status>
    <identifier>user_group</identifier>
    <names>
        <value languageCode="eng-GB">User group</value>
    </names>
    <descriptions/>
    <creationDate>2002-06-18T11:21:38+02:00</creationDate>
    <modificationDate>2019-02-25T14:41:53+01:00</modificationDate>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/3/groups"/>
    <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/3/draft"/>
    <remoteId>25b4268cdcd01921b808a0d854b877ef</remoteId>
    <urlAliasSchema></urlAliasSchema>
    <nameSchema>&lt;name&gt;</nameSchema>
    <isContainer>true</isContainer>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <defaultAlwaysAvailable>true</defaultAlwaysAvailable>
    <defaultSortField>PATH</defaultSortField>
    <defaultSortOrder>ASC</defaultSortOrder>
</ContentTypeInfo>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to create the draft

##### 403

Error - A Content Type with the given new identifier already exists. A draft already exists.

### Delete Content Type

Deletes the provided Content Type

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/content/types/{contentTypeId}`   | 
| Method                             | DELETE                             | 

#### Responses

##### 204

No Content - Content Type deleted

##### 401

Error - The user is not authorized to delete this Content Type

##### 403

Error - There are object instances of this Content Type. The response should contain an ErrorMessage.

##### 404

Error - The Content Type does not exist

### Get Field Definition

Returns the Field definition given by ID

| Parameter                                              | Value                                                  | 
| ------------------------------------------------------ | ------------------------------------------------------ | 
| URI                                                    | `/content/types/{contentTypeId}/{fieldDefinitionId}`   | 
| Method                                                 | GET                                                    | 

#### Headers

##### Accept

If set the Field definition is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.FieldDefinition+xml`<br>`application/vnd.ez.api.FieldDefinition+json`<br>``   | 

#### Responses

##### 200

OK - returns the Field definition

###### Payload

##### application/vnd.ez.api.FieldDefinition+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | FieldDefinition   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/15/fieldDefinitions/195">
    <id>195</id>
    <identifier>title</identifier>
    <fieldType>ezstring</fieldType>
    <fieldGroup></fieldGroup>
    <position>1</position>
    <isTranslatable>true</isTranslatable>
    <isRequired>true</isRequired>
    <isInfoCollector>false</isInfoCollector>
    <defaultValue>New article</defaultValue>
    <isSearchable>true</isSearchable>
    <names>
        <value languageCode="eng-GB">Title</value>
    </names>
    <descriptions/>
    <fieldSettings/>
    <validatorConfiguration>
        <value key="StringLengthValidator">
            <value key="maxStringLength">255</value>
            <value key="minStringLength"/></value>
    </validatorConfiguration>
</FieldDefinition>
```

##### 401

Error - The user is not authorized to read the Content Type

##### 404

Error - The Content Type does not exist

### Update Draft

Updates metadata of a draft. This method does not handle Field definitions. PATCH or POST with header X-HTTP-Method-Override PATCH.

| Parameter                                | Value                                    | 
| ---------------------------------------- | ---------------------------------------- | 
| URI                                      | `/content/types/{contentTypeId}/draft`   | 
| Method                                   | PATCH                                    | 

#### Headers

##### Accept

If set the new Content Type draft is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.ContentTypeInfo+xml`<br>`application/vnd.ez.api.ContentTypeInfo+json`<br>``   | 

##### Content-Type

The Content Type Update schema encoded in XML or JSON

| Parameter                                                                                                 | Value                                                                                                     | 
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                      | string                                                                                                    | 
| Default                                                                                                   | n/a                                                                                                       | 
| Required                                                                                                  | no                                                                                                        | 
| Example                                                                                                   | `application/vnd.ez.api.ContentTypeUpdate+xml`<br>`application/vnd.ez.api.ContentTypeUpdate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.ContentTypeUpdate+xml

| Parameter           | Value               | 
| ------------------- | ------------------- | 
| Type                | ContentTypeUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeUpdate>
    <names>
        <value languageCode="eng-GB">Updated Content Type name</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">This is an updated Content Type description</value>
    </descriptions>
</ContentTypeUpdate>
```

#### Responses

##### 200

Draft metadata updated

###### Payload

##### application/vnd.ez.api.ContentTypeInfo+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | ContentTypeInfo   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeInfo media-type="application/vnd.ez.api.ContentTypeInfo+xml" href="/api/ezp/v2/content/types/14/draft">
    <id>14</id>
    <status>DRAFT</status>
    <identifier>new_content_type</identifier>
    <names>
        <value languageCode="eng-GB">Updated Content Type name</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">This is an updated Content Type description</value>
    </descriptions>
    <creationDate>2019-02-06T10:56:36+01:00</creationDate>
    <modificationDate>2019-02-25T12:15:51+01:00</modificationDate>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/14/groups"/>
    <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/14/draft"/>
    <remoteId>d7ae816f22fe929e67a359a2ef6e7cde</remoteId>
    <urlAliasSchema></urlAliasSchema>
    <nameSchema>&lt;short_title|title&gt;</nameSchema>
    <isContainer>true</isContainer>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
    <defaultSortField>PATH</defaultSortField>
    <defaultSortOrder>ASC</defaultSortOrder>
</ContentTypeInfo>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to update the draft

##### 403

Error - A Content Type with the given new identifier already exists

##### 404

Error - There is no draft for this Content Type

### Publish content type

Publishes a Content Type draft. PUBLISH or POST with header X-HTTP-Method-Override PUBLISH.

| Parameter                                | Value                                    | 
| ---------------------------------------- | ---------------------------------------- | 
| URI                                      | `/content/types/{contentTypeId}/draft`   | 
| Method                                   | PUBLISH                                  | 

#### Responses

##### 200

Content Type draft published

###### Payload

##### application/vnd.ez.api.ContentType+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | ContentType   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/14">
    <id>14</id>
    <status>DEFINED</status>
    <identifier>copy_of_article_14</identifier>
    <names>
        <value languageCode="eng-GB">Updated Content Type name</value>
    </names>
    <descriptions>
        <value languageCode="eng-GB">This is an updated Content Type description</value>
    </descriptions>
    <creationDate>2019-02-06T10:56:36+01:00</creationDate>
    <modificationDate>2019-02-25T12:15:51+01:00</modificationDate>
    <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Modifier media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <Groups media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/types/14/groups"/>
    <Draft media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/14/draft"/>
    <remoteId>d7ae816f22fe929e67a359a2ef6e7cde</remoteId>
    <urlAliasSchema></urlAliasSchema>
    <nameSchema>&lt;short_title|title&gt;</nameSchema>
    <isContainer>true</isContainer>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <defaultAlwaysAvailable>false</defaultAlwaysAvailable>
    <defaultSortField>PATH</defaultSortField>
    <defaultSortOrder>ASC</defaultSortOrder>
    <FieldDefinitions media-type="application/vnd.ez.api.FieldDefinitionList+xml" href="/api/ezp/v2/content/types/14/fieldDefinitions">
        <FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/14/fieldDefinitions/188">
            <id>188</id>
            <identifier>title</identifier>
            <fieldType>ezstring</fieldType>
            <fieldGroup></fieldGroup>
            <position>1</position>
            <isTranslatable>true</isTranslatable>
            <isRequired>true</isRequired>
            <isInfoCollector>false</isInfoCollector>
            <defaultValue>New article</defaultValue>
            <isSearchable>true</isSearchable>
            <names>
                <value languageCode="eng-GB">Title</value>
            </names>
            <descriptions/>
            <fieldSettings/>
            <validatorConfiguration>
                <value key="StringLengthValidator">
                    <value key="maxStringLength">255</value>
                    <value key="minStringLength"/></value>
            </validatorConfiguration>
        </FieldDefinition>
        </FieldDefinitions>
</ContentType>
```

##### 401

Error - The user is not authorized to publish this Content Type draft

##### 403

Error - The Content Type draft is not complete, e.g. there is no Field definition provided

##### 404

Error - If there is no draft or Content Type with the given ID

### Delete Content Type Draft

Deletes the provided Content Type draft

| Parameter                                | Value                                    | 
| ---------------------------------------- | ---------------------------------------- | 
| URI                                      | `/content/types/{contentTypeId}/draft`   | 
| Method                                   | DELETE                                   | 

#### Responses

##### 204

No Content - Content Type draft deleted

##### 401

Error - The user is not authorized to delete this Content Type draft

##### 404

Error - The Content Type/draft does not exist

### Add Field Definition

Creates a new Field definition for the given Content Type

| Parameter                                                 | Value                                                     | 
| --------------------------------------------------------- | --------------------------------------------------------- | 
| URI                                                       | `/content/types/{contentTypeId}/draft/fieldDefinitions`   | 
| Method                                                    | POST                                                      | 

#### Headers

##### Accept

If set the new Field definition is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.FieldDefinition+xml`<br>`application/vnd.ez.api.FieldDefinition+json`<br>``   | 

##### Content-Type

The Field Definition Create schema encoded in XML or JSON

| Parameter                                                                                                         | Value                                                                                                             | 
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                              | string                                                                                                            | 
| Default                                                                                                           | n/a                                                                                                               | 
| Required                                                                                                          | no                                                                                                                | 
| Example                                                                                                           | `application/vnd.ez.api.FieldDefinitionCreate+xml`<br>`application/vnd.ez.api.FieldDefinitionCreate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.FieldDefinitionCreate+xml

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| Type                    | FieldDefinitionCreate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FieldDefinitionCreate>
    <identifier>name</identifier>
    <fieldType>ezstring</fieldType>
    <isRequired>true</isRequired>
    <validatorConfiguration>
    <value key="StringLengthValidator">
        <value key="maxStringLength">32</value>
        <value key="minStringLength">8</value>
    </value>
</validatorConfiguration>
</FieldDefinitionCreate>
```

#### Responses

##### 201

Field definition created

###### Payload

##### application/vnd.ez.api.FieldDefinition+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | FieldDefinition   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/14/draft/fieldDefinitions/221">
    <id>221</id>
    <identifier>name2</identifier>
    <fieldType>ezstring</fieldType>
    <fieldGroup></fieldGroup>
    <position>0</position>
    <isTranslatable>true</isTranslatable>
    <isRequired>true</isRequired>
    <isInfoCollector>false</isInfoCollector>
    <defaultValue/>
    <isSearchable>true</isSearchable>
    <names/>
    <descriptions/>
    <fieldSettings/>
    <validatorConfiguration>
        <value key="StringLengthValidator">
            <value key="maxStringLength">32</value>
            <value key="minStringLength">8</value>
        </value>
    </validatorConfiguration>
</FieldDefinition>
```

##### 400

Error - The input does not match the input schema definition or validation on the field definition fails. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to add a Field definition

##### 403

Error - A Field definition with same identifier already exists in the given Content Type. The Field definition is of singular type, already existing in the given Content Type. The Field definition ti add is of a type that can't be added to a Content Type that already has content instances

### Get Field Definition

Returns the Field definition given by ID

| Parameter                                                                     | Value                                                                         | 
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | 
| URI                                                                           | `/content/types/{contentTypeId}/draft/fieldDefinitions/{fieldDefinitionId}`   | 
| Method                                                                        | GET                                                                           | 

#### Headers

##### Accept

If set the Field definition is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.FieldDefinition+xml`<br>`application/vnd.ez.api.FieldDefinition+json`<br>``   | 

#### Responses

##### 200

OK - returns the Field definition

###### Payload

##### application/vnd.ez.api.FieldDefinition+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | FieldDefinition   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/15/draft/fieldDefinitions/195">
    <id>195</id>
    <identifier>title</identifier>
    <fieldType>ezstring</fieldType>
    <fieldGroup></fieldGroup>
    <position>1</position>
    <isTranslatable>true</isTranslatable>
    <isRequired>true</isRequired>
    <isInfoCollector>false</isInfoCollector>
    <defaultValue>New article</defaultValue>
    <isSearchable>true</isSearchable>
    <names>
        <value languageCode="eng-GB">Title</value>
    </names>
    <descriptions/>
    <fieldSettings/>
    <validatorConfiguration>
        <value key="StringLengthValidator">
            <value key="maxStringLength">255</value>
            <value key="minStringLength"/></value>
    </validatorConfiguration>
</FieldDefinition>
```

##### 401

Error - The user is not authorized to read the Content Type draft

##### 404

Error - The Content Type or draft does not exist

### Update Field definition

Updates the attributes of a Field definition

| Parameter                                                                     | Value                                                                         | 
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | 
| URI                                                                           | `/content/types/{contentTypeId}/draft/fieldDefinitions/{fieldDefinitionId}`   | 
| Method                                                                        | PATCH                                                                         | 

#### Headers

##### Accept

If set the updated Field definition is returned in XML or JSON format

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.FieldDefinition+xml`<br>`application/vnd.ez.api.FieldDefinition+json`<br>``   | 

##### Content-Type

The Field Definition Update schema encoded in XML or JSON

| Parameter                                                                                                         | Value                                                                                                             | 
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                              | string                                                                                                            | 
| Default                                                                                                           | n/a                                                                                                               | 
| Required                                                                                                          | no                                                                                                                | 
| Example                                                                                                           | `application/vnd.ez.api.FieldDefinitionUpdate+xml`<br>`application/vnd.ez.api.FieldDefinitionUpdate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.FieldDefinitionUpdate+xml

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| Type                    | FieldDefinitionUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FieldDefinitionUpdate>
    <fieldGroup>new_field_group</fieldGroup>
    <position>10</position>
</FieldDefinitionUpdate>
```

#### Responses

##### 200

OK - attributes updated

###### Payload

##### application/vnd.ez.api.FieldDefinition+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | FieldDefinition   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FieldDefinition media-type="application/vnd.ez.api.FieldDefinition+xml" href="/api/ezp/v2/content/types/15/draft/fieldDefinitions/197">
    <id>197</id>
    <identifier>author</identifier>
    <fieldType>ezauthor</fieldType>
    <fieldGroup>new_field_group</fieldGroup>
    <position>10</position>
    <isTranslatable>true</isTranslatable>
    <isRequired>false</isRequired>
    <isInfoCollector>false</isInfoCollector>
    <defaultValue/>
    <isSearchable>false</isSearchable>
    <names>
        <value languageCode="eng-GB">Author</value>
    </names>
    <descriptions/>
    <fieldSettings>
        <value key="defaultAuthor">1</value>
    </fieldSettings>
    <validatorConfiguration/>
</FieldDefinition>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to update the Field definition

##### 403

Error - A Field definition with the given new identifier already exists in the given Content Type.

### Delete Field Definition

Deletes the provided Field definition

| Parameter                                                                     | Value                                                                         | 
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | 
| URI                                                                           | `/content/types/{contentTypeId}/draft/fieldDefinitions/{fieldDefinitionId}`   | 
| Method                                                                        | DELETE                                                                        | 

#### Responses

##### 204

No Content - Field definition deleted

##### 401

Error - The user is not authorized to delete this Content Type

##### 403

Error - There is no draft of the Content Type assigned to the authenticated user

### Get Groups of Content Type

Returns the Content Type Group the Content Type belongs to.

| Parameter                                 | Value                                     | 
| ----------------------------------------- | ----------------------------------------- | 
| URI                                       | `/content/types/{contentTypeId}/groups`   | 
| Method                                    | GET                                       | 

#### Headers

##### Accept

If set the Content Type Group list is returned in XML or JSON format

| Parameter                                                                                                             | Value                                                                                                                 | 
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                  | string                                                                                                                | 
| Default                                                                                                               | n/a                                                                                                                   | 
| Required                                                                                                              | no                                                                                                                    | 
| Example                                                                                                               | `application/vnd.ez.api.ContentTypeGroupRefList+xml`<br>`application/vnd.ez.api.ContentTypeGroupRefList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.ContentTypeGroupRefList+xml

| Parameter                 | Value                     | 
| ------------------------- | ------------------------- | 
| Type                      | ContentTypeGroupRefList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroupRefList media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/typegroups/12/types">
    <ContentTypeGroupRef media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/3"/>
</ContentTypeGroupRefList>
```

##### 401

Error - The user is not authorized to read this Content Type

##### 404

Error - The Content Type does not exist

### Link Group to Content Type

Links a Content Type Group to the Content Type and returns the updated group list

| Parameter                                 | Value                                     | 
| ----------------------------------------- | ----------------------------------------- | 
| URI                                       | `/content/types/{contentTypeId}/groups`   | 
| Method                                    | POST                                      | 

#### Headers

##### Accept

If set the updated Content Type Group list is returned in XML or JSON format

| Parameter                                                                                                             | Value                                                                                                                 | 
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                  | string                                                                                                                | 
| Default                                                                                                               | n/a                                                                                                                   | 
| Required                                                                                                              | no                                                                                                                    | 
| Example                                                                                                               | `application/vnd.ez.api.ContentTypeGroupRefList+xml`<br>`application/vnd.ez.api.ContentTypeGroupRefList+json`<br>``   | 

#### Query Parameters

| Name                                                              | Type                                                              | Default                                                           | Required                                                          | Example                                                           | Description                                                       | 
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | 
| group                                                             | string                                                            | n/a                                                               | no                                                                | n/a                                                               | The uri of the group to which the Content Type should be linked   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.ContentTypeGroupRefList+xml

| Parameter                 | Value                     | 
| ------------------------- | ------------------------- | 
| Type                      | ContentTypeGroupRefList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroupRefList media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/typegroups/15/types">
    <ContentTypeGroupRef media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/1">
        <unlink href="/api/ezp/v2/content/types/15/groups/1" method="DELETE"/>
    </ContentTypeGroupRef>
    <ContentTypeGroupRef media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/3">
        <unlink href="/api/ezp/v2/content/types/15/groups/3" method="DELETE"/>
    </ContentTypeGroupRef>
    <ContentTypeGroupRef media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/2">
        <unlink href="/api/ezp/v2/content/types/15/groups/2" method="DELETE"/>
    </ContentTypeGroupRef>
</ContentTypeGroupRefList>
```

##### 400

Error - The input does not match the input schema definition. In this case the response contains an ErrorMessage

##### 401

Error - The user is not authorized to add a group

##### 403

Error - The Content Type is already assigned to the group

### Unlink Group from Content Type

Removes the given group from the Content Type and returns the updated group list

| Parameter                                      | Value                                          | 
| ---------------------------------------------- | ---------------------------------------------- | 
| URI                                            | `/content/types/{contentTypeId}/groups/{id}`   | 
| Method                                         | DELETE                                         | 

#### Headers

##### Accept

If set the updated Content Type Group list is returned in XML or JSON format

| Parameter                                                                                                             | Value                                                                                                                 | 
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                  | string                                                                                                                | 
| Default                                                                                                               | n/a                                                                                                                   | 
| Required                                                                                                              | no                                                                                                                    | 
| Example                                                                                                               | `application/vnd.ez.api.ContentTypeGroupRefList+xml`<br>`application/vnd.ez.api.ContentTypeGroupRefList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.ContentTypeGroup+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | ContentTypeGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentTypeGroupRefList media-type="application/vnd.ez.api.ContentTypeGroupRefList+xml" href="/api/ezp/v2/content/typegroups/15/types">
    <ContentTypeGroupRef media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/1">
        <unlink href="/api/ezp/v2/content/types/15/groups/1" method="DELETE"/>
    </ContentTypeGroupRef>
    <ContentTypeGroupRef media-type="application/vnd.ez.api.ContentTypeGroup+xml" href="/api/ezp/v2/content/typegroups/2">
        <unlink href="/api/ezp/v2/content/types/15/groups/2" method="DELETE"/>
    </ContentTypeGroupRef>
</ContentTypeGroupRefList>
```

##### 401

Error - The user is not authorized to delete this Content Type

##### 403

Error - Content Type cannot be unlinked from the only remaining group

##### 404

Error - The resource does not exist

## Views

### Create View

Executes a query and returns view including the results the View input reflects the criteria model of the public API

| Parameter   | Value       | 
| ----------- | ----------- | 
| URI         | `/views`    | 
| Method      | POST        | 

#### Headers

##### Accept

The view in XML or JSON format

| Parameter                                                                                                                                                                            | Value                                                                                                                                                                                | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | 
| Type                                                                                                                                                                                 | string                                                                                                                                                                               | 
| Default                                                                                                                                                                              | n/a                                                                                                                                                                                  | 
| Required                                                                                                                                                                             | no                                                                                                                                                                                   | 
| Example                                                                                                                                                                              | `application/vnd.ez.api.View+xml`<br>`application/vnd.ez.api.View+json`<br>`application/vnd.ez.api.View+xml; version=1.1`<br>`application/vnd.ez.api.View+json; version=1.1`<br>``   | 

##### Content-Type

The view input in XML or JSON format

| Parameter                                                                                                                                                                                                | Value                                                                                                                                                                                                    | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                                                     | string                                                                                                                                                                                                   | 
| Default                                                                                                                                                                                                  | n/a                                                                                                                                                                                                      | 
| Required                                                                                                                                                                                                 | no                                                                                                                                                                                                       | 
| Example                                                                                                                                                                                                  | `application/vnd.ez.api.ViewInput+xml`<br>`application/vnd.ez.api.ViewInput+json`<br>`application/vnd.ez.api.ViewInput+xml; version=1.1`<br>`application/vnd.ez.api.ViewInput+json; version=1.1`<br>``   | 

#### Payload

##### application/vnd.ez.api.ViewInput+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | ViewInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ViewInput>
  <identifier>TitleView</identifier>
  <ContentQuery>
    <Filter>
      <ContentTypeIdentifierCriterion>image</ContentTypeIdentifierCriterion>
      <SectionIdentifierCriterion>media</SectionIdentifierCriterion>
    </Filter>
    <limit>10</limit>
    <offset>0</offset>
    <SortClauses>
      <ContentName>ascending</ContentName>
    </SortClauses>
    <FacetBuilders>
      <contentTypeFacetBuilder/>
    </FacetBuilders>
  </ContentQuery>
</ViewInput>
```

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.View+xml; version=1.1

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | View        | 

```
<?xml version="1.0" encoding="UTF-8"?>
<View href="/views/TitleView" media-type="application/vnd.ez.api.View+xml; version=1.1">
  <identifier>TitleView</identifier>
  <User href="/user/users/14" media-type="vnd.ez.api.User+xml"/>
  <public>false</public>
  <LocationQuery>
    <Filter>
      <ParentLocationIdCriterion>2</ParentLocationIdCriterion>
    </Filter>
    <limit>10</limit>
    <offset>0</offset>
    <SortClauses>
      <ContentName>ascending</ContentName>
    </SortClauses>
    <FacetBuilders>
      <contentTypeFacetBuilder/>
    </FacetBuilders>
  </LocationQuery>
  <Result href="/content/views/view1234/results"
    media-type="application/vnd.ez.api.ViewResult+xml" count="34" time="31" maxScore="1.0">
    <searchHits>
      <searchHit score="1.0" index="installid1234567890">
        <hightlight/>
        <value>
          <Location media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/2">
            <id>2</id>
            <priority>0</priority>
            <hidden>false</hidden>
            <invisible>false</invisible>
            <ParentLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1"/>
            <pathString>/1/2/</pathString>
            <depth>1</depth>
            <childCount>8</childCount>
            <remoteId>f3e90596361e31d496d4026eb624c983</remoteId>
            <Children media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/locations/1/2/children"/>
            <Content media-type="application/vnd.ez.api.Content+xml" href="/api/ezp/v2/content/objects/57"/>
            <sortField>PRIORITY</sortField>
            <sortOrder>ASC</sortOrder>
            <UrlAliases media-type="application/vnd.ez.api.UrlAliasRefList+xml" href="/api/ezp/v2/content/locations/1/2/urlaliases"/>
          </Location>

        </value>
      </searchHit>
      <!-- ... -->
    </searchHits>
    <facets>
      <contentTypeFacet>
        <contentTypeFacetEntry>
          <contentType href="/content/types/1"  media-type="application/vnd.ez.api.ContentType+xml"/>
          <count>3</count>
        </contentTypeFacetEntry>
        <contentTypeFacetEntry>
          <contentType href="/content/types/7"  media-type="application/vnd.ez.api.ContentType+xml"/>
          <count>9</count>
        </contentTypeFacetEntry>
        <contentTypeFacetEntry>
          <contentType href="/content/types/11"  media-type="application/vnd.ez.api.ContentType+xml"/>
          <count>1</count>
        </contentTypeFacetEntry>
        <contentTypeFacetEntry>
          <contentType href="/content/types/15"  media-type="application/vnd.ez.api.ContentType+xml"/>
          <count>8</count>
        </contentTypeFacetEntry>
      </contentTypeFacet>
    </facets>
  </Result>
</View>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

## Managing users

### Load User Groups

Load user groups for either an ID or remoteId or role.

| Parameter        | Value            | 
| ---------------- | ---------------- | 
| URI              | `/user/groups`   | 
| Method           | GET              | 

#### Headers

##### Accept

UserGroupList - if set the user group list is returned in XML or JSON format. UserGroupRefList - if set the link list of user groups is returned in XML or JSON format

| Parameter                                                                                                                                                                                            | Value                                                                                                                                                                                                | 
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                                                 | string                                                                                                                                                                                               | 
| Default                                                                                                                                                                                              | n/a                                                                                                                                                                                                  | 
| Required                                                                                                                                                                                             | no                                                                                                                                                                                                   | 
| Example                                                                                                                                                                                              | `application/vnd.ez.api.UserGroupList+xml`<br>`application/vnd.ez.api.UserGroupList+json`<br>`application/vnd.ez.api.UserGroupRefList+xml`<br>`application/vnd.ez.api.UserGroupRefList+json`<br>``   | 

#### Query Parameters

| Name                                              | Type                                              | Default                                           | Required                                          | Example                                           | Description                                       | 
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | 
| roleId                                            | string                                            | n/a                                               | no                                                | n/a                                               | Lists user groups assigned to the given role      | 
| id                                                | string                                            | n/a                                               | no                                                | n/a                                               | Retrieves the user group for the given ID         | 
| remoteID                                          | string                                            | n/a                                               | no                                                | n/a                                               | Retrieves the user group for the given remoteId   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.UserGroupList+xml

| Parameter       | Value           | 
| --------------- | --------------- | 
| Type            | UserGroupList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserGroupList media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/groups">
<UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/13/15" id="14" remoteId="1bb4fe25487f05527efa8bfd394cecc7">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/4"/>
    <name>Administrator User</name>
    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/14/versions"/>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
    <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/13/15"/>
    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/14/locations"/>
    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <publishDate>2002-10-06T18:13:50+02:00</publishDate>
    <lastModificationDate>2011-03-25T15:07:04+01:00</lastModificationDate>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <alwaysAvailable>true</alwaysAvailable>
    <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/14/versions/3">
        <VersionInfo>
            <id>499</id>
            <versionNo>3</versionNo>
            <status>PUBLISHED</status>
            <modificationDate>2011-03-25T15:07:04+01:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2011-03-25T15:03:03+01:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">Administrator User</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/14"/>
        </VersionInfo>
        <Fields>
            <field>
                <id>28</id>
                <fieldDefinitionIdentifier>first_name</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                <fieldValue>Administrator</fieldValue>
            </field>
            <field>
                <id>29</id>
                <fieldDefinitionIdentifier>last_name</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                <fieldValue>User</fieldValue>
            </field>
            <field>
                <id>30</id>
                <fieldDefinitionIdentifier>user_account</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezuser</fieldTypeIdentifier>
                <fieldValue>
                    <value key="hasStoredLogin">true</value>
                    <value key="contentId">14</value>
                    <value key="login">admin</value>
                    <value key="email">nospam@ez.no</value>
                    <value key="enabled">true</value>
                    <value key="maxLogin">10</value>
                </fieldValue>
            </field>
            <field>
                <id>178</id>
                <fieldDefinitionIdentifier>signature</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>eztext</fieldTypeIdentifier>
                <fieldValue/>
            </field>
            <field>
                <id>180</id>
                <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezimage</fieldTypeIdentifier>
                <fieldValue/>
            </field>
        </Fields>
        <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/14/versions/3/relations"/>
    </Version>
    <ParentUserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/13"/>
    <Subgroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/groups/1/5/13/15/subgroups"/>
    <Users media-type="application/vnd.ez.api.UserList+xml" href="/api/ezp/v2/user/groups/1/5/13/15/users"/>
    <Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/13/15/roles"/>
</UserGroup>
</UserGroupList>
```

##### 401

Error - the user has no permission to read user groups

### Get Root User Group

Redirects to the root user group

| Parameter             | Value                 | 
| --------------------- | --------------------- | 
| URI                   | `/user/groups/root`   | 
| Method                | GET                   | 

#### Responses

##### 301

Moved permanently.

### Load User Group

Loads user groups for the given {path}

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/user/groups/{path}`   | 
| Method                  | GET                     | 

#### Headers

##### Accept

If set the new user group is returned in XML or JSON format

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.UserGroup+xml`<br>`application/vnd.ez.api.UserGroup+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - loads user groups

###### Payload

##### application/vnd.ez.api.UserGroup+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UserGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/14" id="13" remoteId="3c160cca19fb135f83bd02d911f04db2">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/3"/>
    <name>Editors</name>
    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/13/versions"/>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
    <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/14"/>
    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/13/locations"/>
    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <publishDate>2002-10-06T18:13:14+02:00</publishDate>
    <lastModificationDate>2002-10-06T18:13:14+02:00</lastModificationDate>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <alwaysAvailable>true</alwaysAvailable>
    <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/13/versions/1">
        <VersionInfo>
            <id>441</id>
            <versionNo>1</versionNo>
            <status>PUBLISHED</status>
            <modificationDate>2002-10-06T18:13:14+02:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2002-10-06T18:13:06+02:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">Editors</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/13"/>
        </VersionInfo>
        <Fields>
            <field>
                <id>26</id>
                <fieldDefinitionIdentifier>name</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                <fieldValue>Editors</fieldValue>
            </field>
            <field>
                <id>27</id>
                <fieldDefinitionIdentifier>description</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                <fieldValue/>
            </field>
        </Fields>
        <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/13/versions/1/relations"/>
    </Version>
    <ParentUserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5"/>
    <Subgroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/groups/1/5/14/subgroups"/>
    <Users media-type="application/vnd.ez.api.UserList+xml" href="/api/ezp/v2/user/groups/1/5/14/users"/>
    <Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/14/roles"/>
</UserGroup>
```

##### 401

Error - the user has no permission to read user groups

##### 404

Error -	if the user group does not exist

### Update User Group

Updates a user group - PATCH or POST with header X-HTTP-Method-Override PATCH

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/user/groups/{path}`   | 
| Method                  | PATCH                   | 

#### Headers

##### Accept

If set the new user group is returned in XML or JSON forma

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.UserGroup+xml`<br>`application/vnd.ez.api.UserGroup+json`<br>``   | 

##### Content-Type

The UserGroupUpdate schema encoded in XML or JSON

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.UserGroupUpdate+json`<br>`application/vnd.ez.api.UserGroupUpdate+xml`<br>``   | 

##### If-Match

Causes to patch only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | `ETag`      | 

#### Payload

##### application/vnd.ez.api.UserGroupUpdate+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | UserGroupUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserGroupUpdate>
	<Section href="/api/ezp/v2/content/sections/3" />
</UserGroupUpdate>
```

#### Responses

##### 200

OK - updated user group

###### Payload

##### application/vnd.ez.api.UserGroup+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UserGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
 <UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/65" id="57" remoteId="9819b9739e775b69f8d791cdc6cb4c34">
     <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/3"/>
     <name>Editors</name>
     <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/57/versions"/>
     <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
     <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/65"/>
     <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/57/locations"/>
     <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
     <publishDate>2019-02-27T09:58:39+01:00</publishDate>
     <lastModificationDate>2019-02-27T09:58:39+01:00</lastModificationDate>
     <mainLanguageCode>eng-GB</mainLanguageCode>
     <alwaysAvailable>true</alwaysAvailable>
     <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/57/versions/1">
         <VersionInfo>
             <id>512</id>
             <versionNo>1</versionNo>
             <status>PUBLISHED</status>
             <modificationDate>2019-02-27T09:58:39+01:00</modificationDate>
             <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
             <creationDate>2019-02-27T09:58:39+01:00</creationDate>
             <initialLanguageCode>eng-GB</initialLanguageCode>
             <languageCodes>eng-GB</languageCodes>
             <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                 <Language>
                     <languageCode>eng-GB</languageCode>
                 </Language>
             </VersionTranslationInfo>
             <names>
                 <value languageCode="eng-GB">Editors</value>
             </names>
             <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/57"/>
         </VersionInfo>
         <Fields>
             <field>
                 <id>203</id>
                 <fieldDefinitionIdentifier>name</fieldDefinitionIdentifier>
                 <languageCode>eng-GB</languageCode>
                 <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                 <fieldValue>Editors</fieldValue>
             </field>
             <field>
                 <id>204</id>
                 <fieldDefinitionIdentifier>description</fieldDefinitionIdentifier>
                 <languageCode>eng-GB</languageCode>
                 <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                 <fieldValue>editors</fieldValue>
             </field>
         </Fields>
         <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/57/versions/1/relations"/>
     </Version>
     <ParentUserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5"/>
     <Subgroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/groups/1/5/65/subgroups"/>
     <Users media-type="application/vnd.ez.api.UserList+xml" href="/api/ezp/v2/user/groups/1/5/65/users"/>
     <Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/65/roles"/>
 </UserGroup>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to update the user group

##### 412

Error -	if the current ETag does not match with the provided one in the If-Match header

### Delete User Group

The given user group is deleted

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/user/groups/{path}`   | 
| Method                  | DELETE                  | 

#### Responses

##### 204

No content - the given user group is deleted

##### 401

Error - the user is not authorized to delete this Content Type

##### 403

Error - the user group is not empty

### Move user Group

Moves the user group to another parent. MOVE or POST with header X-HTTP-Method-Override MOVE

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/user/groups/{path}`   | 
| Method                  | MOVE                    | 

#### Headers

##### Destination

A parent group resource to which the Location is moved

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 201

Created - moves the user group to another parent

##### 401

Error - the user is not authorized to update the user group

##### 403

Error - the new parent does not exist

##### 404

Error - the user group does not exist

### Create User

Creates a new user in the given group

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/user/groups/{path}/users`   | 
| Method                        | POST                          | 

#### Headers

##### Accept

If set the new user is returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.User+xml`<br>`application/vnd.ez.api.User+json`<br>``   | 

##### Content-Type

The UserCreate schema encoded in XML or JSON

| Parameter                                                                                   | Value                                                                                       | 
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | 
| Type                                                                                        | string                                                                                      | 
| Default                                                                                     | n/a                                                                                         | 
| Required                                                                                    | no                                                                                          | 
| Example                                                                                     | `application/vnd.ez.api.UserCreate+json`<br>`application/vnd.ez.api.UserCreate+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.UserCreate+xml

| Parameter    | Value        | 
| ------------ | ------------ | 
| Type         | UserCreate   | 

```xml
examples/user/groups/path/users/POST/UserCreate.xml.example
```

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.User+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | User        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/59" id="59" remoteId="remoteId-qwert426">
<ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/4"/>
<name>Yura Rajzer</name>
<Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/59/versions"/>
<Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
<MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/65/67"/>
<Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/59/locations"/>
<Groups media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/users/59/groups"/>
<Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
<publishDate>2019-02-27T11:23:42+01:00</publishDate>
<lastModificationDate>2019-02-27T11:23:42+01:00</lastModificationDate>
<mainLanguageCode>eng-GB</mainLanguageCode>
<alwaysAvailable>true</alwaysAvailable>
<Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/59/versions/1">
    <VersionInfo>
        <id>515</id>
        <versionNo>1</versionNo>
        <status>PUBLISHED</status>
        <modificationDate>2019-02-27T11:23:42+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <creationDate>2019-02-27T11:23:42+01:00</creationDate>
        <initialLanguageCode>eng-GB</initialLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
            <Language>
                <languageCode>eng-GB</languageCode>
            </Language>
        </VersionTranslationInfo>
        <names>
            <value languageCode="eng-GB">Yura Rajzer</value>
        </names>
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/59"/>
    </VersionInfo>
    <Fields>
        <field>
            <id>207</id>
            <fieldDefinitionIdentifier>first_name</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>Yura</fieldValue>
        </field>
        <field>
            <id>208</id>
            <fieldDefinitionIdentifier>last_name</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>Rajzer</fieldValue>
        </field>
        <field>
            <id>209</id>
            <fieldDefinitionIdentifier>user_account</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezuser</fieldTypeIdentifier>
            <fieldValue>
                <value key="hasStoredLogin">true</value>
                <value key="contentId">59</value>
                <value key="login">yura</value>
                <value key="email">yurarajzer@example.net</value>
                <value key="enabled">true</value>
                <value key="maxLogin">0</value>
            </fieldValue>
        </field>
        <field>
            <id>210</id>
            <fieldDefinitionIdentifier>signature</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>eztext</fieldTypeIdentifier>
            <fieldValue/>
        </field>
        <field>
            <id>211</id>
            <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezimage</fieldTypeIdentifier>
            <fieldValue/>
        </field>
    </Fields>
    <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/59/versions/1/relations"/>
</Version>
<login>yura</login>
<email>yurarajzer@example.net</email>
<enabled>true</enabled>
<UserGroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/users/59/groups"/>
<Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/users/59/roles"/>
</User>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to create this user

##### 403

Error - a user with the same login already exists

##### 404

Error - the group with the given ID does not exist

### Create User Group

Creates a new user group under the given parent. To create a top level group use /user/groups/subgroups

| Parameter                         | Value                             | 
| --------------------------------- | --------------------------------- | 
| URI                               | `/user/groups/{path}/subgroups`   | 
| Method                            | POST                              | 

#### Headers

##### Accept

If set the new user group is returned in XML or JSON format

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.UserGroup+xml`<br>`application/vnd.ez.api.UserGroup+json`<br>``   | 

##### Content-Type

The UserGroupCreate schema encoded in XML or JSON

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.UserGroupCreate+json`<br>`application/vnd.ez.api.UserGroupCreate+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.UserGroupCreate+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | UserGroupCreate   | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.UserGroup+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UserGroup   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/65/68" id="60" remoteId="remoteId-qwert098">
<ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/3"/>
<name>UserGroup</name>
<Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/60/versions"/>
<Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
<MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/65/68"/>
<Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/60/locations"/>
<Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
<publishDate>2019-02-27T11:45:38+01:00</publishDate>
<lastModificationDate>2019-02-27T11:45:38+01:00</lastModificationDate>
<mainLanguageCode>eng-GB</mainLanguageCode>
<alwaysAvailable>true</alwaysAvailable>
<Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/60/versions/1">
    <VersionInfo>
        <id>516</id>
        <versionNo>1</versionNo>
        <status>PUBLISHED</status>
        <modificationDate>2019-02-27T11:45:38+01:00</modificationDate>
        <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <creationDate>2019-02-27T11:45:38+01:00</creationDate>
        <initialLanguageCode>eng-GB</initialLanguageCode>
        <languageCodes>eng-GB</languageCodes>
        <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
            <Language>
                <languageCode>eng-GB</languageCode>
            </Language>
        </VersionTranslationInfo>
        <names>
            <value languageCode="eng-GB">UserGroup</value>
        </names>
        <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/60"/>
    </VersionInfo>
    <Fields>
        <field>
            <id>212</id>
            <fieldDefinitionIdentifier>name</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>UserGroup</fieldValue>
        </field>
        <field>
            <id>213</id>
            <fieldDefinitionIdentifier>description</fieldDefinitionIdentifier>
            <languageCode>eng-GB</languageCode>
            <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
            <fieldValue>This is the description of the user group</fieldValue>
        </field>
    </Fields>
    <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/60/versions/1/relations"/>
</Version>
<ParentUserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/65"/>
<Subgroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/groups/1/5/65/68/subgroups"/>
<Users media-type="application/vnd.ez.api.UserList+xml" href="/api/ezp/v2/user/groups/1/5/65/68/users"/>
<Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/65/68/roles"/>
</UserGroup>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to create this user group

### Load Roles for User Group

Returns a list of all roles assigned to the given user group

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/user/groups/{path}/roles`   | 
| Method                        | GET                           | 

#### Headers

##### Accept

If set the Role assignment list is returned in XML or JSON format

| Parameter                                                                                                   | Value                                                                                                       | 
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                        | string                                                                                                      | 
| Default                                                                                                     | n/a                                                                                                         | 
| Required                                                                                                    | no                                                                                                          | 
| Example                                                                                                     | `application/vnd.ez.api.RoleAssignmentList+xml`<br>`application/vnd.ez.api.RoleAssignmentList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RoleAssignmentList+xml

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| Type                 | RoleAssignmentList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignmentList media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/65/roles">
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/groups/1/5/65/roles/3">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/3"/>
</RoleAssignment>
</RoleAssignmentList>
```

##### 400

Error - the user has no permission to read roles

### Assigns a Role to a user group.

Assigns a Role to a user group.

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/user/groups/{path}/roles`   | 
| Method                        | POST                          | 

#### Headers

##### Accept

If set the updated Role assignment list is returned in XML or JSON format

| Parameter                                                                                                   | Value                                                                                                       | 
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                        | string                                                                                                      | 
| Default                                                                                                     | n/a                                                                                                         | 
| Required                                                                                                    | no                                                                                                          | 
| Example                                                                                                     | `application/vnd.ez.api.RoleAssignmentList+xml`<br>`application/vnd.ez.api.RoleAssignmentList+json`<br>``   | 

##### Content-Type

The RoleAssignInput schema encoded in XML or JSON

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.RoleAssignInput+json`<br>`application/vnd.ez.api.RoleAssignInput+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.RoleAssignInput+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | RoleAssignInput   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RoleAssignmentList+xml

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| Type                 | RoleAssignmentList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignmentList media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/65/roles">
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/groups/1/5/65/roles/3">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/3"/>
</RoleAssignment>
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/groups/1/5/65/roles/10">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/10"/>
</RoleAssignment>
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/groups/1/5/65/roles/10">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="4"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/10"/>
</RoleAssignment>
</RoleAssignmentList>
```

##### 400

Error - validation of limitation in RoleAssignInput fails

##### 401

Error - the user is not authorized to assign this role

### Load Assignment

Returns a Role assignment of the given user group

| Parameter                              | Value                                  | 
| -------------------------------------- | -------------------------------------- | 
| URI                                    | `/user/groups/{path}/roles/{roleId}`   | 
| Method                                 | GET                                    | 

#### Headers

##### Accept

If set the Role assignment list is returned in XML or JSON format

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.RoleAssignment+xml`<br>`application/vnd.ez.api.RoleAssignment+json`<br>``   | 

#### Responses

##### 200

OK - returns a roleassignment of the given user group

###### Payload

##### application/vnd.ez.api.RoleAssignment+xml

| Parameter        | Value            | 
| ---------------- | ---------------- | 
| Type             | RoleAssignment   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/groups/1/5/65/roles/10">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/10"/>
</RoleAssignment>
```

##### 401

Error - the user has no permission to read roles

### Unassign Role from User Group

The given Role is removed from the user or user group

| Parameter                              | Value                                  | 
| -------------------------------------- | -------------------------------------- | 
| URI                                    | `/user/groups/{path}/roles/{roleId}`   | 
| Method                                 | DELETE                                 | 

#### Headers

##### Accept

If set the updated Role assignment list is returned in XML or JSON format

| Parameter                                                                                                   | Value                                                                                                       | 
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                        | string                                                                                                      | 
| Default                                                                                                     | n/a                                                                                                         | 
| Required                                                                                                    | no                                                                                                          | 
| Example                                                                                                     | `application/vnd.ez.api.RoleAssignmentList+xml`<br>`application/vnd.ez.api.RoleAssignmentList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RoleAssignmentList+xml

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| Type                 | RoleAssignmentList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignmentList media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/groups/1/5/65/roles">
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/groups/1/5/65/roles/3">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/3"/>
</RoleAssignment>
</RoleAssignmentList>
```

##### 401

Error - the user is not authorized to delete this Role assignment

### Load Users of Group

Loads the users of the group with the given ID

| Parameter                   | Value                       | 
| --------------------------- | --------------------------- | 
| URI                         | `/user/groups/{id}/users`   | 
| Method                      | GET                         | 

#### Headers

##### Accept

UserList - if set the user list returned in XML or JSON format. UserRefList - if set the link list of users returned in XML or JSON format

| Parameter                                                                                                                                                                        | Value                                                                                                                                                                            | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                             | string                                                                                                                                                                           | 
| Default                                                                                                                                                                          | n/a                                                                                                                                                                              | 
| Required                                                                                                                                                                         | no                                                                                                                                                                               | 
| Example                                                                                                                                                                          | `application/vnd.ez.api.UserList+xml`<br>`application/vnd.ez.api.UserList+json`<br>`application/vnd.ez.api.UserRefList+xml`<br>`application/vnd.ez.api.UserRefList+json`<br>``   | 

#### Query Parameters

| Name                                                    | Type                                                    | Default                                                 | Required                                                | Example                                                 | Description                                             | 
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | 
| limit                                                   | string                                                  | n/a                                                     | no                                                      | n/a                                                     | Only 'limit' items will be returned started by offset   | 
| offset                                                  | string                                                  | n/a                                                     | no                                                      | n/a                                                     | Offset of the result set                                | 

#### Responses

##### 200

OK - the users of the group with the given ID

###### Payload

##### application/vnd.ez.api.UserRefList+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | UserRefList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserRefList media-type="application/vnd.ez.api.UserRefList+xml" href="/api/ezp/v2/user/groups/65/users">
    <User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/55"/>
    <User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/59"/>
</UserRefList>
```

##### 401

Error - the user has no permission to read user groups

##### 404

Error - the user group does not exist

### Load Subgroups

Returns a list of the sub groups

| Parameter                       | Value                           | 
| ------------------------------- | ------------------------------- | 
| URI                             | `/user/groups/{id}/subgroups`   | 
| Method                          | GET                             | 

#### Headers

##### Accept

UserGroupList - if set the user group list returned in XML or JSON format. UserGroupRefList - if set the link list of user groups is returned in XML or JSON format

| Parameter                                                                                                                                                                                            | Value                                                                                                                                                                                                | 
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                                                 | string                                                                                                                                                                                               | 
| Default                                                                                                                                                                                              | n/a                                                                                                                                                                                                  | 
| Required                                                                                                                                                                                             | no                                                                                                                                                                                                   | 
| Example                                                                                                                                                                                              | `application/vnd.ez.api.UserGroupList+xml`<br>`application/vnd.ez.api.UserGroupList+json`<br>`application/vnd.ez.api.UserGroupRefList+xml`<br>`application/vnd.ez.api.UserGroupRefList+json`<br>``   | 

#### Query Parameters

| Name                               | Type                               | Default                            | Required                           | Example                            | Description                        | 
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | 
| limit                              | string                             | n/a                                | no                                 | n/a                                | The number of locations returned   | 
| offset                             | string                             | n/a                                | no                                 | n/a                                | The offset of the result set       | 

#### Responses

##### 200

OK - list of the sub groups

###### Payload

##### application/vnd.ez.api.UserGroupRefList+xml

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | UserGroupRefList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserGroupRefList media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/groups/65/subgroups">
    <UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/65/68"/>
</UserGroupRefList>
```

##### 401

Error - the user has no permission to read user groups

##### 404

Error - the user group does not exist

### List Users

Load users either for a given remoteId or role

| Parameter       | Value           | 
| --------------- | --------------- | 
| URI             | `/user/users`   | 
| Method          | GET             | 

#### Headers

##### Accept

UserList - if set the user list returned in XML or JSON format. UserRefList - if set the link list of users returned in XML or JSON format

| Parameter                                                                                                                                                                        | Value                                                                                                                                                                            | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                             | string                                                                                                                                                                           | 
| Default                                                                                                                                                                          | n/a                                                                                                                                                                              | 
| Required                                                                                                                                                                         | no                                                                                                                                                                               | 
| Example                                                                                                                                                                          | `application/vnd.ez.api.UserList+xml`<br>`application/vnd.ez.api.UserList+json`<br>`application/vnd.ez.api.UserRefList+xml`<br>`application/vnd.ez.api.UserRefList+json`<br>``   | 

#### Query Parameters

| Name                                                                                                         | Type                                                                                                         | Default                                                                                                      | Required                                                                                                     | Example                                                                                                      | Description                                                                                                  | 
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | 
| roleId                                                                                                       | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Lists users assigned to the given Role (e.g. GET /user/users?roleId=/user/roles/1)                           | 
| remoteId                                                                                                     | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Retrieves the user for the given remoteId (e.g. GET /user/users?remoteId=55dd9713db75145f374bbd0b4f60ad29)   | 
| login                                                                                                        | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Retrieves the user for the given login (e.g. GET /user/users?login=editor)                                   | 
| email                                                                                                        | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Lists users with the given email (e.g. GET /user/users?email=editor@example.com)                             | 

#### Responses

##### 200

OK - Loads users either for a given remoteId or role

###### Payload

##### application/vnd.ez.api.UserRefList+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | UserRefList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserRefList media-type="application/vnd.ez.api.UserRefList+xml" href="/api/ezp/v2/user/users">
    <User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
</UserRefList>
```

##### application/vnd.ez.api.UserList+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UserList    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserList media-type="application/vnd.ez.api.UserList+xml" href="/api/ezp/v2/user/users">
    <User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14" id="14" remoteId="1bb4fe25487f05527efa8bfd394cecc7">
        <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/4"/>
        <name>Administrator User</name>
        <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/14/versions"/>
        <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
        <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/13/15"/>
        <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/14/locations"/>
        <Groups media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/users/14/groups"/>
        <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <publishDate>2002-10-06T18:13:50+02:00</publishDate>
        <lastModificationDate>2011-03-25T15:07:04+01:00</lastModificationDate>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <alwaysAvailable>true</alwaysAvailable>
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/14/versions/3">
            <VersionInfo>
                <id>499</id>
                <versionNo>3</versionNo>
                <status>PUBLISHED</status>
                <modificationDate>2011-03-25T15:07:04+01:00</modificationDate>
                <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                <creationDate>2011-03-25T15:03:03+01:00</creationDate>
                <initialLanguageCode>eng-GB</initialLanguageCode>
                <languageCodes>eng-GB</languageCodes>
                <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                    <Language>
                        <languageCode>eng-GB</languageCode>
                    </Language>
                </VersionTranslationInfo>
                <names>
                    <value languageCode="eng-GB">Administrator User</value>
                </names>
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/14"/>
            </VersionInfo>
            <Fields>
                <field>
                    <id>28</id>
                    <fieldDefinitionIdentifier>first_name</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>Administrator</fieldValue>
                </field>
                <field>
                    <id>29</id>
                    <fieldDefinitionIdentifier>last_name</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>User</fieldValue>
                </field>
                <field>
                    <id>30</id>
                    <fieldDefinitionIdentifier>user_account</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezuser</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="hasStoredLogin">true</value>
                        <value key="contentId">14</value>
                        <value key="login">admin</value>
                        <value key="email">nospam@ez.no</value>
                        <value key="enabled">true</value>
                        <value key="maxLogin">10</value>
                    </fieldValue>
                </field>
                <field>
                    <id>178</id>
                    <fieldDefinitionIdentifier>signature</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>eztext</fieldTypeIdentifier>
                    <fieldValue/>
                </field>
                <field>
                    <id>180</id>
                    <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezimage</fieldTypeIdentifier>
                    <fieldValue/>
                </field>
            </Fields>
            <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/14/versions/3/relations"/>
        </Version>
        <login>admin</login>
        <email>nospam@ez.no</email>
        <enabled>true</enabled>
        <UserGroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/users/14/groups"/>
        <Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/users/14/roles"/>
    </User>
</UserList>
```

##### 404

If there are no visibile users matching the filter

### Verify users

Verifies if there are users matching the given filter.

| Parameter       | Value           | 
| --------------- | --------------- | 
| URI             | `/user/users`   | 
| Method          | HEAD            | 

#### Query Parameters

| Name                                                                                                         | Type                                                                                                         | Default                                                                                                      | Required                                                                                                     | Example                                                                                                      | Description                                                                                                  | 
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | 
| roleId                                                                                                       | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Lists users assigned to the given Role (e.g. GET /user/users?roleId=/user/roles/1)                           | 
| remoteId                                                                                                     | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Retrieves the user for the given remoteId (e.g. GET /user/users?remoteId=55dd9713db75145f374bbd0b4f60ad29)   | 
| login                                                                                                        | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Retrieves the user for the given login (e.g. GET /user/users?login=editor)                                   | 
| email                                                                                                        | string                                                                                                       | n/a                                                                                                          | no                                                                                                           | n/a                                                                                                          | Lists users with the given email (e.g. GET /user/users?email=editor@example.com)                             | 

#### Responses

##### 200

OK - verifies if there are users matching the given filter

##### 404

Error - there are no visibile users matching the filter

### Loade user

Loads the user with the given ID

| Parameter                | Value                    | 
| ------------------------ | ------------------------ | 
| URI                      | `/user/users/{userId}`   | 
| Method                   | GET                      | 

#### Headers

##### Accept

If set the user is returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.User+xml`<br>`application/vnd.ez.api.User+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - the user with the given ID

###### Payload

##### application/vnd.ez.api.User+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | UserList    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserList media-type="application/vnd.ez.api.UserList+xml" href="/api/ezp/v2/user/users">
    <User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/55" id="55" remoteId="3c1d660927760cc2b812526735c52539">
        <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/4"/>
        <name>Jessica Andaya</name>
        <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/55/versions"/>
        <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
        <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/14/62"/>
        <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/55/locations"/>
        <Groups media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/users/55/groups"/>
        <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
        <publishDate>2019-02-27T08:46:07+01:00</publishDate>
        <lastModificationDate>2019-02-27T08:46:07+01:00</lastModificationDate>
        <mainLanguageCode>eng-GB</mainLanguageCode>
        <alwaysAvailable>true</alwaysAvailable>
        <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/55/versions/1">
            <VersionInfo>
                <id>510</id>
                <versionNo>1</versionNo>
                <status>PUBLISHED</status>
                <modificationDate>2019-02-27T08:46:08+01:00</modificationDate>
                <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
                <creationDate>2019-02-27T08:46:07+01:00</creationDate>
                <initialLanguageCode>eng-GB</initialLanguageCode>
                <languageCodes>eng-GB</languageCodes>
                <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                    <Language>
                        <languageCode>eng-GB</languageCode>
                    </Language>
                </VersionTranslationInfo>
                <names>
                    <value languageCode="eng-GB">Jessica Andaya</value>
                </names>
                <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/55"/>
            </VersionInfo>
            <Fields>
                <field>
                    <id>193</id>
                    <fieldDefinitionIdentifier>first_name</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>Jessica</fieldValue>
                </field>
                <field>
                    <id>194</id>
                    <fieldDefinitionIdentifier>last_name</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                    <fieldValue>Andaya</fieldValue>
                </field>
                <field>
                    <id>195</id>
                    <fieldDefinitionIdentifier>user_account</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezuser</fieldTypeIdentifier>
                    <fieldValue>
                        <value key="hasStoredLogin">true</value>
                        <value key="contentId">55</value>
                        <value key="login">jessica</value>
                        <value key="email">jandaya@example.com</value>
                        <value key="enabled">false</value>
                        <value key="maxLogin">0</value>
                    </fieldValue>
                </field>
                <field>
                    <id>196</id>
                    <fieldDefinitionIdentifier>signature</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>eztext</fieldTypeIdentifier>
                    <fieldValue/>
                </field>
                <field>
                    <id>197</id>
                    <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
                    <languageCode>eng-GB</languageCode>
                    <fieldTypeIdentifier>ezimage</fieldTypeIdentifier>
                    <fieldValue/>
                </field>
            </Fields>
            <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/55/versions/1/relations"/>
        </Version>
        <login>jessica</login>
        <email>jandaya@example.com</email>
        <enabled>false</enabled>
        <UserGroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/users/55/groups"/>
        <Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/users/55/roles"/>
    </User>
</UserList>
```

##### 401

Error - the user has no permission to read users

##### 404

Error - the user does not exist

### Update user

Updates a user

| Parameter                | Value                    | 
| ------------------------ | ------------------------ | 
| URI                      | `/user/users/{userId}`   | 
| Method                   | PATCH                    | 

#### Headers

##### Accept

If set the new user is returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.User+xml`<br>`application/vnd.ez.api.User+json`<br>``   | 

##### Content-Type

The UserUpdate schema encoded in XML or JSON

| Parameter                                                                                   | Value                                                                                       | 
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | 
| Type                                                                                        | string                                                                                      | 
| Default                                                                                     | n/a                                                                                         | 
| Required                                                                                    | no                                                                                          | 
| Example                                                                                     | `application/vnd.ez.api.UserUpdate+json`<br>`application/vnd.ez.api.UserUpdate+xml`<br>``   | 

##### If-Match

Causes to patch only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | `ETag`      | 

#### Payload

##### application/vnd.ez.api.UserUpdate+xml

| Parameter    | Value        | 
| ------------ | ------------ | 
| Type         | UserUpdate   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserUpdate>
  <login>jandaya</login>
  <enabled>false</enabled>
</UserUpdate>
```

#### Responses

##### 200

OK - user updated

###### Payload

##### application/vnd.ez.api.User+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | User        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<User media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/55" id="55" remoteId="3c1d660927760cc2b812526735c52539">
    <ContentType media-type="application/vnd.ez.api.ContentType+xml" href="/api/ezp/v2/content/types/4"/>
    <name>Jessica Andaya</name>
    <Versions media-type="application/vnd.ez.api.VersionList+xml" href="/api/ezp/v2/content/objects/55/versions"/>
    <Section media-type="application/vnd.ez.api.Section+xml" href="/api/ezp/v2/content/sections/2"/>
    <MainLocation media-type="application/vnd.ez.api.Location+xml" href="/api/ezp/v2/content/locations/1/5/14/62"/>
    <Locations media-type="application/vnd.ez.api.LocationList+xml" href="/api/ezp/v2/content/objects/55/locations"/>
    <Groups media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/users/55/groups"/>
    <Owner media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
    <publishDate>2019-02-27T08:46:07+01:00</publishDate>
    <lastModificationDate>2019-02-27T08:46:07+01:00</lastModificationDate>
    <mainLanguageCode>eng-GB</mainLanguageCode>
    <alwaysAvailable>true</alwaysAvailable>
    <Version media-type="application/vnd.ez.api.Version+xml" href="/api/ezp/v2/content/objects/55/versions/1">
        <VersionInfo>
            <id>510</id>
            <versionNo>1</versionNo>
            <status>PUBLISHED</status>
            <modificationDate>2019-02-27T08:46:08+01:00</modificationDate>
            <Creator media-type="application/vnd.ez.api.User+xml" href="/api/ezp/v2/user/users/14"/>
            <creationDate>2019-02-27T08:46:07+01:00</creationDate>
            <initialLanguageCode>eng-GB</initialLanguageCode>
            <languageCodes>eng-GB</languageCodes>
            <VersionTranslationInfo media-type="application/vnd.ez.api.VersionTranslationInfo+xml">
                <Language>
                    <languageCode>eng-GB</languageCode>
                </Language>
            </VersionTranslationInfo>
            <names>
                <value languageCode="eng-GB">Jessica Andaya</value>
            </names>
            <Content media-type="application/vnd.ez.api.ContentInfo+xml" href="/api/ezp/v2/content/objects/55"/>
        </VersionInfo>
        <Fields>
            <field>
                <id>193</id>
                <fieldDefinitionIdentifier>first_name</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                <fieldValue>Jessica</fieldValue>
            </field>
            <field>
                <id>194</id>
                <fieldDefinitionIdentifier>last_name</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezstring</fieldTypeIdentifier>
                <fieldValue>Andaya</fieldValue>
            </field>
            <field>
                <id>195</id>
                <fieldDefinitionIdentifier>user_account</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezuser</fieldTypeIdentifier>
                <fieldValue>
                    <value key="hasStoredLogin">true</value>
                    <value key="contentId">55</value>
                    <value key="login">jessica</value>
                    <value key="email">jandaya@example.com</value>
                    <value key="enabled">false</value>
                    <value key="maxLogin">0</value>
                </fieldValue>
            </field>
            <field>
                <id>196</id>
                <fieldDefinitionIdentifier>signature</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>eztext</fieldTypeIdentifier>
                <fieldValue/>
            </field>
            <field>
                <id>197</id>
                <fieldDefinitionIdentifier>image</fieldDefinitionIdentifier>
                <languageCode>eng-GB</languageCode>
                <fieldTypeIdentifier>ezimage</fieldTypeIdentifier>
                <fieldValue/>
            </field>
        </Fields>
        <Relations media-type="application/vnd.ez.api.RelationList+xml" href="/api/ezp/v2/content/objects/55/versions/1/relations"/>
    </Version>
    <login>jessica</login>
    <email>jandaya@example.com</email>
    <enabled>false</enabled>
    <UserGroups media-type="application/vnd.ez.api.UserGroupList+xml" href="/api/ezp/v2/user/users/55/groups"/>
    <Roles media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/users/55/roles"/>
</User>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to update the user

##### 404

Error - the user does not exist

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

### Delete user

The given user is deleted

| Parameter                | Value                    | 
| ------------------------ | ------------------------ | 
| URI                      | `/user/users/{userId}`   | 
| Method                   | DELETE                   | 

#### Responses

##### 204

No Content

##### 401

Error - the user is not authorized to delete this user

##### 403

Error - the user is the same as the authenticated user

##### 404

Error - the user does not exist

### Load Groups Of User

Returns a list of user groups the user belongs to. The returned list includes the resources for unassigning a user group if the user is in multiple groups.

| Parameter                       | Value                           | 
| ------------------------------- | ------------------------------- | 
| URI                             | `/user/users/{userId}/groups`   | 
| Method                          | GET                             | 

#### Headers

##### Accept

If set the link list of user groups is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.UserGroupRefList+xml`<br>`application/vnd.ez.api.UserGroupRefList+json`<br>``   | 

#### Query Parameters

| Name                               | Type                               | Default                            | Required                           | Example                            | Description                        | 
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | 
| offset                             | integer                            | n/a                                | no                                 | n/a                                | The offset of the result set       | 
| limit                              | integer                            | n/a                                | no                                 | n/a                                | The number of locations returned   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.UserGroupRefList

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | UserGroupRefList   | 

```
<?xml version="1.0" encoding="UTF-8"?>
<UserGroupRefList media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/users/55/groups">
    <UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/12">
        <unassign href="/api/ezp/v2/user/users/55/groups/12" method="DELETE"/>
    </UserGroup>
    <UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/14">
        <unassign href="/api/ezp/v2/user/users/55/groups/14" method="DELETE"/>
    </UserGroup>
</UserGroupRefList>
```

##### 401

Error - the user has no permission to read user groups

##### 404

Error - the user does not exist

### Assign User Group

Assigns the user to a user group

| Parameter                       | Value                           | 
| ------------------------------- | ------------------------------- | 
| URI                             | `/user/users/{userId}/groups`   | 
| Method                          | POST                            | 

#### Headers

##### Accept

If set the link list of user groups is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.UserGroupRefList+xml`<br>`application/vnd.ez.api.UserGroupRefList+json`<br>``   | 

#### Query Parameters

| Name                                        | Type                                        | Default                                     | Required                                    | Example                                     | Description                                 | 
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | 
| group                                       | string                                      | n/a                                         | no                                          | n/a                                         | The new parent group resource of the user   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.UserGroupRefList

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | UserGroupRefList   | 

```
<?xml version="1.0" encoding="UTF-8"?>
<UserGroupRefList media-type="application/vnd.ez.api.UserGroupRefList+xml" href="/api/ezp/v2/user/users/55/groups">
    <UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/12">
        <unassign href="/api/ezp/v2/user/users/55/groups/12" method="DELETE"/>
    </UserGroup>
    <UserGroup media-type="application/vnd.ez.api.UserGroup+xml" href="/api/ezp/v2/user/groups/1/5/14">
        <unassign href="/api/ezp/v2/user/users/55/groups/14" method="DELETE"/>
    </UserGroup>
</UserGroupRefList>
```

##### 401

Error - the user is not authorized to assign user groups

##### 403

Error - the new user group does not exist or the user is already in this group

##### 404

Error - the user does not exist

### Unassign User Group

Unassigns the user from a user group

| Parameter                                 | Value                                     | 
| ----------------------------------------- | ----------------------------------------- | 
| URI                                       | `/user/users/{userId}/groups/{groupId}`   | 
| Method                                    | DELETE                                    | 

#### Headers

##### Accept

If set the link list of user groups is returned in XML or JSON format

| Parameter                                                                                               | Value                                                                                                   | 
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                    | string                                                                                                  | 
| Default                                                                                                 | n/a                                                                                                     | 
| Required                                                                                                | no                                                                                                      | 
| Example                                                                                                 | `application/vnd.ez.api.UserGroupRefList+xml`<br>`application/vnd.ez.api.UserGroupRefList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.UserGroupRefList

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| Type               | UserGroupRefList   | 

```
<?xml version="1.0" encoding="UTF-8"?>
<UserGroupRefList href="/user/users/45/groups"
  media-type="application/vnd.ez.api.UserGroupRefList">
  <UserGroup href="/user/groups/1/5/34" media-type="application/vnd.ez.api.UserGroup">
    <unassign href="/user/users/45/groups/34" method="DELETE" />
  </UserGroup>
  <UserGroup href="/user/groups/1/5/88" media-type="application/vnd.ez.api.UserGroup">
    <unassign href="/user/users/45/groups/88" method="DELETE" />
  </UserGroup>
</UserGroupRefList>
```

##### 401

Error - the user is not authorized to unassign user groups

##### 403

Error - the user is not in the given group

##### 404

Error - the user does not exist

### Load Roles for User

Returns a list of all roles assigned to the given user

| Parameter                      | Value                          | 
| ------------------------------ | ------------------------------ | 
| URI                            | `/user/users/{userId}/roles`   | 
| Method                         | GET                            | 

#### Headers

##### Accept

If set the Role assignment list is returned in XML or JSON format

| Parameter                                                                                                   | Value                                                                                                       | 
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                        | string                                                                                                      | 
| Default                                                                                                     | n/a                                                                                                         | 
| Required                                                                                                    | no                                                                                                          | 
| Example                                                                                                     | `application/vnd.ez.api.RoleAssignmentList+xml`<br>`application/vnd.ez.api.RoleAssignmentList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RoleAssignmentList+xml

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| Type                 | RoleAssignmentList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignmentList href="/user/groups/1/5/65/roles" media-type="application/vnd.ez.api.RoleAssignmentList+xml">
  <RoleAssignment href="/user/groups/1/5/65/roles/5" media-type="application/vnd.ez.api.RoleAssignment+xml">
    <Role href="/user/roles/5" media-type="application/vnd.ez.api.Role+xml"/>
  </RoleAssignment>
  <RoleAssignment href="/user/groups/1/5/65/roles/7" media-type="application/vnd.ez.api.RoleAssignment+xml">
    <limitation identifier="Subtree">
      <values>
          <ref href="/content/locations/1/23/88" media-type="application/vnd.ez.api.Location+xml" />
          <ref href="/content/locations/1/32/67" media-type="application/vnd.ez.api.Location+xml" />
      </values>
    </limitation>
    <Role href="/user/roles/7" media-type="application/vnd.ez.api.Role+xml"/>
  </RoleAssignment>
</RoleAssignmentList>
```

##### 400

Error - the user has no permission to read roles

### Assign Role to User

Assigns a Role to a user.

| Parameter                      | Value                          | 
| ------------------------------ | ------------------------------ | 
| URI                            | `/user/users/{userId}/roles`   | 
| Method                         | POST                           | 

#### Headers

##### Accept

If set the updated Role assignment list is returned in XML or JSON format

| Parameter                                                                                                   | Value                                                                                                       | 
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                        | string                                                                                                      | 
| Default                                                                                                     | n/a                                                                                                         | 
| Required                                                                                                    | no                                                                                                          | 
| Example                                                                                                     | `application/vnd.ez.api.RoleAssignmentList+xml`<br>`application/vnd.ez.api.RoleAssignmentList+json`<br>``   | 

##### Content-Type

The RoleAssignInput schema encoded in XML or JSON

| Parameter                                                                                             | Value                                                                                                 | 
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | 
| Type                                                                                                  | string                                                                                                | 
| Default                                                                                               | n/a                                                                                                   | 
| Required                                                                                              | no                                                                                                    | 
| Example                                                                                               | `application/vnd.ez.api.RoleAssignInput+json`<br>`application/vnd.ez.api.RoleAssignInput+xml`<br>``   | 

#### Payload

##### application/vnd.ez.api.RoleAssignInput+xml

| Parameter         | Value             | 
| ----------------- | ----------------- | 
| Type              | RoleAssignInput   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RoleAssignmentList+xml

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| Type                 | RoleAssignmentList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignmentList media-type="application/vnd.ez.api.RoleAssignmentList+xml" href="/api/ezp/v2/user/users/55/roles">
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/users/55/roles/10">
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/10"/>
</RoleAssignment>
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/users/55/roles/4">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/4"/>
</RoleAssignment>
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/users/55/roles/4">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="4"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/4"/>
</RoleAssignment>
</RoleAssignmentList>
```

##### 400

Error - validation of limitation in RoleAssignInput fails

##### 401

Error - the user is not authorized to assign this role

### Load Assignment

Returns a Role assignment to the given user group

| Parameter                               | Value                                   | 
| --------------------------------------- | --------------------------------------- | 
| URI                                     | `/user/users/{userId}/roles/{roleId}`   | 
| Method                                  | GET                                     | 

#### Headers

##### Accept

If set the Role assignment list is returned in XML or JSON format

| Parameter                                                                                           | Value                                                                                               | 
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | 
| Type                                                                                                | string                                                                                              | 
| Default                                                                                             | n/a                                                                                                 | 
| Required                                                                                            | no                                                                                                  | 
| Example                                                                                             | `application/vnd.ez.api.RoleAssignment+xml`<br>`application/vnd.ez.api.RoleAssignment+json`<br>``   | 

#### Responses

##### 200

OK - Role assignment to the given user group

###### Payload

##### application/vnd.ez.api.RoleAssignment+xml

| Parameter        | Value            | 
| ---------------- | ---------------- | 
| Type             | RoleAssignment   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignment media-type="application/vnd.ez.api.RoleAssignment+xml" href="/api/ezp/v2/user/users/55/roles/4">
    <limitation identifier="Section">
        <values>
            <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
        </values>
    </limitation>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/4"/>
</RoleAssignment>
```

##### 401

Error - the user has no permission to read roles

### Unassign Role from User

The given Role is removed from the user

| Parameter                               | Value                                   | 
| --------------------------------------- | --------------------------------------- | 
| URI                                     | `/user/users/{userId}/roles/{roleId}`   | 
| Method                                  | DELETE                                  | 

#### Headers

##### Accept

If set the updated Role assignment list is returned in XML or JSON format

| Parameter                                                                                                   | Value                                                                                                       | 
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                        | string                                                                                                      | 
| Default                                                                                                     | n/a                                                                                                         | 
| Required                                                                                                    | no                                                                                                          | 
| Example                                                                                                     | `application/vnd.ez.api.RoleAssignmentList+xml`<br>`application/vnd.ez.api.RoleAssignmentList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.RoleAssignmentList+xml

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| Type                 | RoleAssignmentList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleAssignmentList href="/user/groups/1/5/65/roles" media-type="application/vnd.ez.api.RoleAssignmentList+xml">
  <RoleAssignment href="/user/groups/1/5/65/roles/5" media-type="application/vnd.ez.api.RoleAssignment+xml">
    <Role href="/user/roles/5" media-type="application/vnd.ez.api.Role+xml"/>
  </RoleAssignment>
  <RoleAssignment href="/user/groups/1/5/65/roles/11" media-type="application/vnd.ez.api.RoleAssignment+xml">
    <limitation identifier="Section">
      <values>
          <ref href="/content/sections/1" media-type="application/vnd.ez.api.Section+xml" />
          <ref href="/content/sections/4" media-type="application/vnd.ez.api.Section+xml" />
      </values>
    </limitation>
    <Role href="/user/roles/11" media-type="application/vnd.ez.api.Role+xml"/>
  </RoleAssignment>
</RoleAssignmentList>
```

##### 401

Error - the user is not authorized to delete this Content Type

### Load Roles

Returns a list of all roles

| Parameter       | Value           | 
| --------------- | --------------- | 
| URI             | `/user/roles`   | 
| Method          | GET             | 

#### Headers

##### Accept

If set the user list returned in XML or JSON format

| Parameter                                                                               | Value                                                                                   | 
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | 
| Type                                                                                    | string                                                                                  | 
| Default                                                                                 | n/a                                                                                     | 
| Required                                                                                | no                                                                                      | 
| Example                                                                                 | `application/vnd.ez.api.RoleList+xml`<br>`application/vnd.ez.api.RoleList+json`<br>``   | 

#### Query Parameters

| Name                                                                                                                                | Type                                                                                                                                | Default                                                                                                                             | Required                                                                                                                            | Example                                                                                                                             | Description                                                                                                                         | 
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | 
| identifier                                                                                                                          | string                                                                                                                              | n/a                                                                                                                                 | no                                                                                                                                  | n/a                                                                                                                                 | Restricts the result to a list containing the Role with the given identifier. If the Role is not found an empty list is returned.   | 
| offset                                                                                                                              | integer                                                                                                                             | n/a                                                                                                                                 | no                                                                                                                                  | n/a                                                                                                                                 | The offset of the result set                                                                                                        | 
| limit                                                                                                                               | integer                                                                                                                             | n/a                                                                                                                                 | no                                                                                                                                  | n/a                                                                                                                                 | Only limit items will be returned started by offset                                                                                 | 

#### Responses

##### 200

OK - list of all roles

###### Payload

##### application/vnd.ez.api.RoleList+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | RoleList    | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleList media-type="application/vnd.ez.api.RoleList+xml" href="/api/ezp/v2/user/roles">
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/1">
        <identifier>Anonymous</identifier>
        <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/1/policies"/>
    </Role>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/4">
        <identifier>Member</identifier>
        <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/4/policies"/>
    </Role>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/3">
        <identifier>Editor</identifier>
        <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/3/policies"/>
    </Role>
    <Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/2">
        <identifier>Administrator</identifier>
        <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/2/policies"/>
    </Role>
</RoleList>
```

##### 401

Error - the user has no permission to read roles

### Create Role / Role Draft

Creates a new Role or Role draft

| Parameter       | Value           | 
| --------------- | --------------- | 
| URI             | `/user/roles`   | 
| Method          | POST            | 

#### Headers

##### Accept

If set the new user is returned in XML or JSON format

| Parameter                                                                                                                                                            | Value                                                                                                                                                                | 
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Type                                                                                                                                                                 | string                                                                                                                                                               | 
| Default                                                                                                                                                              | n/a                                                                                                                                                                  | 
| Required                                                                                                                                                             | no                                                                                                                                                                   | 
| Example                                                                                                                                                              | `application/vnd.ez.api.Role+xml`<br>`application/vnd.ez.api.Role+json`<br>`application/vnd.ez.api.RoleDraft+xml`<br>`application/vnd.ez.api.RoleDraft+json`<br>``   | 

##### Content-Type

The RoleInput schema encoded in XML or JSON

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.RoleInput+json`<br>`application/vnd.ez.api.RoleInput+xml`<br>``   | 

#### Query Parameters

| Name                                           | Type                                           | Default                                        | Required                                       | Example                                        | Description                                    | 
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | 
| publish                                        | boolean                                        | 1                                              | no                                             | n/a                                            | If true the role is published after creation   | 

#### Payload

##### application/vnd.ez.api.RoleInput+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | RoleInput   | 

```xml
examples/user/roles/POST/RoleInput.xml.example
```

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.Role+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Role        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/5">
    <identifier>NewRole</identifier>
    <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/5/policies"/>
</Role>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to create this Role / Role draft

### Load Role

Loads a Role for the given ID

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| URI                  | `/user/roles/{id}`   | 
| Method               | GET                  | 

#### Headers

##### Accept

If set the user list returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.Role+xml`<br>`application/vnd.ez.api.Role+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - Role for the given ID

###### Payload

##### application/vnd.ez.api.Role+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Role        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/5">
    <identifier>NewRole</identifier>
    <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/5/policies"/>
</Role>
```

##### 401

Error - the user has no permission to read roles

##### 404

Error - the Role does not exist

### Create Role Draft

Creates a new Role draft from an existing role.

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| URI                  | `/user/roles/{id}`   | 
| Method               | POST                 | 

#### Headers

##### Accept

If set the new user is returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.Role+xml`<br>`application/vnd.ez.api.Role+json`<br>``   | 

##### Content-Type

The RoleInput schema encoded in XML or JSON

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.RoleInput+json`<br>`application/vnd.ez.api.RoleInput+xml`<br>``   | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.RoleDraft+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | RoleDraft   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Role href="/user/roles/11" media-type="application/vnd.ez.api.RoleDraft+xml">
  <identifier>MyRole</identifier>
  <Policies href="/user/roles/11/policies" media-type="application/vnd.ez.api.PolicyList+xml"/>
</Role>
```

##### 401

Error - the user is not authorized to create this Role / Role draft

### Update Role

Updates a role. PATCH or POST with header X-HTTP-Method-Override PATCH

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| URI                  | `/user/roles/{id}`   | 
| Method               | PATCH                | 

#### Headers

##### Accept

If set the new user is returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.Role+xml`<br>`application/vnd.ez.api.Role+json`<br>``   | 

##### Content-Type

The RoleInput schema encoded in XML or JSON

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.RoleInput+json`<br>`application/vnd.ez.api.RoleInput+xml`<br>``   | 

##### If-Match

ETag Causes to patch only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.RoleInput+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | RoleInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleInput>
    <identifier>NewIdentifier</identifier>
</RoleInput>
```

#### Responses

##### 200

OK - role updated

###### Payload

##### application/vnd.ez.api.Role+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Role        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/5">
    <identifier>NewIdentifier</identifier>
    <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/5/policies"/>
</Role>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to update the role

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

### Delete Role

The given Role and all assignments to users or user groups are deleted

| Parameter            | Value                | 
| -------------------- | -------------------- | 
| URI                  | `/user/roles/{id}`   | 
| Method               | DELETE               | 

#### Responses

##### 204

No Content

##### 401

Error - the user is not authorized to delete this role

### Load Role draft

Loads a Role draft by original Role ID

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/user/roles/{id}/draft`   | 
| Method                     | GET                        | 

#### Headers

##### Accept

If set the user list returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.Role+xml`<br>`application/vnd.ez.api.Role+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

OK - Role draft by original Role ID

###### Payload

##### application/vnd.ez.api.Role+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Role        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/9">
    <identifier>Member</identifier>
    <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/9/policies"/>
</Role>
```

##### 401

Error - the user has no permission to read roles

##### 404

Error - there is no draft or Role with the given ID

### Update Role draft

Updates a Role draft. PATCH or POST with header X-HTTP-Method-Override PATCH

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/user/roles/{id}/draft`   | 
| Method                     | PATCH                      | 

#### Headers

##### Accept

If set the updated Role is returned in XML or JSON format

| Parameter                                                                       | Value                                                                           | 
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | 
| Type                                                                            | string                                                                          | 
| Default                                                                         | n/a                                                                             | 
| Required                                                                        | no                                                                              | 
| Example                                                                         | `application/vnd.ez.api.Role+xml`<br>`application/vnd.ez.api.Role+json`<br>``   | 

##### Content-Type

The RoleInput schema encoded in XML or JSON

| Parameter                                                                                 | Value                                                                                     | 
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | 
| Type                                                                                      | string                                                                                    | 
| Default                                                                                   | n/a                                                                                       | 
| Required                                                                                  | no                                                                                        | 
| Example                                                                                   | `application/vnd.ez.api.RoleInput+json`<br>`application/vnd.ez.api.RoleInput+xml`<br>``   | 

##### If-Match

ETag Causes to patch only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.RoleInput+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | RoleInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<RoleInput>
    <identifier>UpdatedIdentifier</identifier>
</RoleInput>
```

#### Responses

##### 200

OK - Role draft updated

###### Payload

##### application/vnd.ez.api.Role+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Role        | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Role media-type="application/vnd.ez.api.Role+xml" href="/api/ezp/v2/user/roles/9">
    <identifier>UpdatedIdentifier</identifier>
    <Policies media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/roles/9/policies"/>
</Role>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the user is not authorized to update the role

##### 404

Error - there is no draft or Role with the given ID

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

### Publish Role draft

Publishes a Role draft. PUBLISH or POST with header X-HTTP-Method-Override PUBLISH

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/user/roles/{id}/draft`   | 
| Method                     | PUBLISH                    | 

#### Responses

##### 204

No Content

##### 401

Error - the user is not authorized to publish this Content Type draft

##### 403

Error - the Content Type draft is not complete e.g. there is no field definition provided

##### 404

Error - there is no draft or Role with the given ID

### Delete Role Draft

The given Role draft is deleted.

| Parameter                  | Value                      | 
| -------------------------- | -------------------------- | 
| URI                        | `/user/roles/{id}/draft`   | 
| Method                     | DELETE                     | 

#### Responses

##### 204

No Content

##### 401

Error - the user is not authorized to delete this role

### Load Policies

Loads policies for the given role

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/user/roles/{id}/policies`   | 
| Method                        | GET                           | 

#### Headers

##### Accept

If set the Policy list is returned in XML or JSON format

| Parameter                                                                                   | Value                                                                                       | 
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | 
| Type                                                                                        | string                                                                                      | 
| Default                                                                                     | n/a                                                                                         | 
| Required                                                                                    | no                                                                                          | 
| Example                                                                                     | `application/vnd.ez.api.PolicyList+xml`<br>`application/vnd.ez.api.PolicyList+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.PolicyList+xml

| Parameter    | Value        | 
| ------------ | ------------ | 
| Type         | PolicyList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<PolicyList href="/user/roles/11/policies" media-type="application/vnd.ez.api.PolicyList">
  <Policy href="/user/roles/11/policies/45" media-type="application/vnd.ez.api.Policy+xml">
    <id>45</id>
    <module>content</module>
    <function>create</function>
    <limitations>
      <limitation identifier="Class">
        <values>
          <ref href="/content/types/10" media-type="application/vnd.ez.api.ContentType+xml" />
          <ref href="/content/types/11" media-type="application/vnd.ez.api.ContentType+xml" />
          <ref href="/content/types/12" media-type="application/vnd.ez.api.ContentType+xml" />
        </values>
      </limitation>
      <limitation identifier="ParentClass">
        <values>
          <ref href="/content/types/4" media-type="application/vnd.ez.api.ContentType+xml" />
        </values>
      </limitation>
    </limitations>
  </Policy>
  <Policy href="/user/roles/11/policies/49" media-type="application/vnd.ez.api.Policy+xml">
    <id>49</id>
    <module>content</module>
    <function>read</function>
    <limitations>
      <limitation identifier="Section">
        <values>
          <ref href="/content/sections/1" media-type="application/vnd.ez.api.Section+xml" />
          <ref href="/content/sections/2" media-type="application/vnd.ez.api.Section+xml" />
          <ref href="/content/sections/4" media-type="application/vnd.ez.api.Section+xml" />
        </values>
      </limitation>
    </limitations>
  </Policy>
</PolicyList>
```

##### 401

Error - the user has no permission to read roles

##### 404

Error - the Role does not exist

### Delete Policies

All policies of the given Role are deleted

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/user/roles/{id}/policies`   | 
| Method                        | DELETE                        | 

#### Responses

##### 204

No Content - all policies of the given Role are deleted

##### 401

Error - the user is not authorized to delete this Content Type

### Create Policy

Creates a policy

| Parameter                     | Value                         | 
| ----------------------------- | ----------------------------- | 
| URI                           | `/user/roles/{id}/policies`   | 
| Method                        | POST                          | 

#### Headers

##### Accept

If set the updated Policy is returned in XML or JSON format

| Parameter                                                                           | Value                                                                               | 
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | 
| Type                                                                                | string                                                                              | 
| Default                                                                             | n/a                                                                                 | 
| Required                                                                            | no                                                                                  | 
| Example                                                                             | `application/vnd.ez.api.Policy+xml`<br>`application/vnd.ez.api.Policy+json`<br>``   | 

##### Content-Type

If set the updated Policy is returned in XML or JSON format

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.PolicyCreate+xml`<br>`application/vnd.ez.api.PolicyCreate+json`<br>``   | 

#### Payload

##### application/vnd.ez.api.PolicyCreate+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | PolicyCreate   | 

#### Responses

##### 201

###### Payload

##### application/vnd.ez.api.Policy+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Policy      | 

```xml
<Policy href="/user/roles/11/policies/55" media-type="application/vnd.ez.api.Policy+xml">
  <id>55</id>
  <module>content</module>
  <function>create</function>
  <limitations>
    <limitation identifier="Class">
      <values>
        <ref href="/content/types/13"/>
      </values>
    </limitation>
    <limitation identifier="ParentClass">
      <values>
        <ref href="/content/types/12"/>
      </values>
    </limitation>
  </limitations>
 </Policy>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage OR validation of limitation in PolicyCreate fails

##### 401

Error - the user is not authorized to create the policy

##### 404

Error - the Role does not exist

### Update Policy

Updates a policy. PATCH or POST with header X-HTTP-Method-Override PATCH

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/user/roles/{id}/policies/{id}`   | 
| Method                             | PATCH                              | 

#### Headers

##### Accept

If set the updated Policy is returned in XML or JSON format

| Parameter                                                                           | Value                                                                               | 
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | 
| Type                                                                                | string                                                                              | 
| Default                                                                             | n/a                                                                                 | 
| Required                                                                            | no                                                                                  | 
| Example                                                                             | `application/vnd.ez.api.Policy+xml`<br>`application/vnd.ez.api.Policy+json`<br>``   | 

##### Content-Type

If set the updated Policy is returned in XML or JSON format

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.PolicyUpdate+xml`<br>`application/vnd.ez.api.PolicyUpdate+json`<br>``   | 

##### If-Match

Causes to patch only if the specified ETag is the current one. Otherwise a 412 is returned.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | `ETag`      | 

#### Payload

##### application/vnd.ez.api.PolicyUpdate+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | PolicyUpdate   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Policy+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Policy      | 

```xml
<Policy href="/user/roles/11/policies/55" media-type="application/vnd.ez.api.Policy+xml">
  <id>55</id>
  <module>content</module>
  <function>create</function>
  <limitations>
    <limitation identifier="Class">
      <values>
        <ref href="/content/types/14"/>
      </values>
    </limitation>
    <limitation identifier="ParentClass">
      <values>
        <ref href="/content/types/10"/>
      </values>
    </limitation>
  </limitations>
 </Policy>
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage OR validation of limitation in PolicyUpdate fails

##### 401

Error - the user is not authorized to update the policy

##### 404

Error - the Role does not exist

##### 412

Error - the current ETag does not match with the provided one in the If-Match header

### Load Policy

Loads a Policy for the given module and function

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/user/roles/{id}/policies/{id}`   | 
| Method                             | GET                                | 

#### Headers

##### Accept

If set the Policy is returned in XML or JSON format

| Parameter                                                                           | Value                                                                               | 
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | 
| Type                                                                                | string                                                                              | 
| Default                                                                             | n/a                                                                                 | 
| Required                                                                            | no                                                                                  | 
| Example                                                                             | `application/vnd.ez.api.Policy+xml`<br>`application/vnd.ez.api.Policy+json`<br>``   | 

##### If-None-Match

ETag

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Policy+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Policy      | 

```xml
<Policy href="/user/roles/11/policies/45" media-type="application/vnd.ez.api.Policy+xml">
  <id>45</id>
  <module>content</module>
  <function>create</function>
  <limitations>
    <limitation identifier="Class">
      <values>
        <ref href="/content/types/10" media-type="application/vnd.ez.api.ContentType+xml" />
        <ref href="/content/types/11" media-type="application/vnd.ez.api.ContentType+xml" />
        <ref href="/content/types/12" media-type="application/vnd.ez.api.ContentType+xml" />
      </values>
    </limitation>
    <limitation identifier="ParentClass">
      <values>
        <ref href="/content/types/4" media-type="application/vnd.ez.api.ContentType+xml" />
      </values>
    </limitation>
  </limitations>
</Policy>
```

##### 401

Error - the user has no permission to read roles

##### 404

Error - the Role or Policy does not exist

### Delete Policy

The given Policy is deleted

| Parameter                          | Value                              | 
| ---------------------------------- | ---------------------------------- | 
| URI                                | `/user/roles/{id}/policies/{id}`   | 
| Method                             | DELETE                             | 

#### Responses

##### 204

No Content - the given Policy is deleted

##### 401

Error - the user is not authorized to delete this Content Type

##### 404

Error - the Role or Policy does not exist

### List Policies for user

Search all policies which are applied to a given user

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/user/policies`   | 
| Method             | GET                | 

#### Headers

##### Accept

If set the Policy list is returned in XML or JSON format

| Parameter                                                                                   | Value                                                                                       | 
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | 
| Type                                                                                        | string                                                                                      | 
| Default                                                                                     | n/a                                                                                         | 
| Required                                                                                    | no                                                                                          | 
| Example                                                                                     | `application/vnd.ez.api.PolicyList+xml`<br>`application/vnd.ez.api.PolicyList+json`<br>``   | 

#### Query Parameters

| Name          | Type          | Default       | Required      | Example       | Description   | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | 
| userId        | string        | n/a           | no            | n/a           | The user ID   | 

#### Responses

##### 200

OK - policies which are applied to a given user

###### Payload

##### application/vnd.ez.api.PolicyList+xml

| Parameter    | Value        | 
| ------------ | ------------ | 
| Type         | PolicyList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<PolicyList media-type="application/vnd.ez.api.PolicyList+xml" href="/api/ezp/v2/user/policies">
    <Policy media-type="application/vnd.ez.api.Policy+xml" href="/api/ezp/v2/user/roles/1/policies/328">
        <id>328</id>
        <module>content</module>
        <function>read</function>
        <limitations>
            <limitation identifier="Section">
                <values>
                    <ref media-type="application/vnd.ez.api.ref+xml" href="1"/>
                </values>
            </limitation>
        </limitations>
    </Policy>
    <Policy media-type="application/vnd.ez.api.Policy+xml" href="/api/ezp/v2/user/roles/1/policies/331">
        <id>331</id>
        <module>user</module>
        <function>login</function>
        <limitations>
            <limitation identifier="SiteAccess">
                <values>
                    <ref media-type="application/vnd.ez.api.ref+xml" href="1766001124"/>
                </values>
            </limitation>
        </limitations>
    </Policy>
</PolicyList>
```

##### 401

Error - the user has no permission to read roles

### Create session (login a User)

Performs a login for the user or check if session exists and returns the session and session cookie. The client will need to remember both session name/ID and CSRF token as this is for security reasons not exposed via GET.

| Parameter          | Value              | 
| ------------------ | ------------------ | 
| URI                | `/user/sessions`   | 
| Method             | POST               | 

#### Headers

##### Accept

If set the Session is returned in XML or JSON format

| Parameter                                                                             | Value                                                                                 | 
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | 
| Type                                                                                  | string                                                                                | 
| Default                                                                               | n/a                                                                                   | 
| Required                                                                              | no                                                                                    | 
| Example                                                                               | `application/vnd.ez.api.Session+xml`<br>`application/vnd.ez.api.Session+json`<br>``   | 

##### Content-Type

The SessionInput schema encoded in XML or JSON

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.SessionInput+xml`<br>`application/vnd.ez.api.SessionInput+json`<br>``   | 

##### Cookie

Only needed for session's checking {sessionName}={sessionID}

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

##### X-CSRF-Token

Only needed for session's checking. The {csrfToken} needed on all unsafe http methods with session.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Payload

##### application/vnd.ez.api.SessionInput+xml

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | SessionInput   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SessionInput>
  <login>admin</login>
  <password>secret</password>
</SessionInput>
```

##### application/vnd.ez.api.SessionInput+json

| Parameter      | Value          | 
| -------------- | -------------- | 
| Type           | SessionInput   | 

```json
{
  "SessionInput": {
    "login": "admin",
    "password": "secret"
  }
}
```

#### Responses

##### 200

If session already exists

###### Payload

##### application/vnd.ez.api.Session+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Session     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Session href="/user/sessions/sessionID" media-type="application/vnd.ez.api.Session+xml">
  <name>eZSSID</name>
  <identifier>go327ij2cirpo59pb6rrv2a4el2</identifier>
  <csrfToken>23lkneri34ijajedfw39orj3j93</csrfToken>
  <User href="/user/users/14" media-type="vnd.ez.api.User+xml"/>
</Session>
```

##### application/vnd.ez.api.Session+json

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Session     | 

```json
{
  "Session": {
    "name": "eZSSID",
    "identifier": "go327ij2cirpo59pb6rrv2a4el2",
    "csrfToken": "23lkneri34ijajedfw39orj3j93",
    "User": {
      "_href": "/user/users/14",
      "_media-type": "application/vnd.ez.api.User+json"
    }
  }
}
```

##### 201

If session is created

###### Payload

##### application/vnd.ez.api.Session+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Session     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Session href="/user/sessions/sessionID" media-type="application/vnd.ez.api.Session+xml">
  <name>eZSSID</name>
  <identifier>go327ij2cirpo59pb6rrv2a4el2</identifier>
  <csrfToken>23lkneri34ijajedfw39orj3j93</csrfToken>
  <User href="/user/users/14" media-type="vnd.ez.api.User+xml"/>
</Session>
```

##### application/vnd.ez.api.Session+json

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Session     | 

```json
{
  "Session": {
    "name": "eZSSID",
    "identifier": "go327ij2cirpo59pb6rrv2a4el2",
    "csrfToken": "23lkneri34ijajedfw39orj3j93",
    "User": {
      "_href": "/user/users/14",
      "_media-type": "application/vnd.ez.api.User+json"
    }
  }
}
```

##### 400

Error - the Input does not match the input schema definition, In this case the response contains an ErrorMessage

##### 401

Error - the authorization failed

##### 409

Error - header contained a session cookie but different user was authorized

### Delete session (logout a User)

The user session is removed i.e. the user is logged out.

| Parameter                      | Value                          | 
| ------------------------------ | ------------------------------ | 
| URI                            | `/user/sessions/{sessionId}`   | 
| Method                         | DELETE                         | 

#### Headers

##### Cookie

{sessionName}={essionID}

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

##### X-CSRF-Token

The {csrfToken} needed on all unsafe http methods with session.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 204

OK - Session deleted

##### 404

Error - the session does not exist

### Refresh session (get session's User information)

Give the session's User information

| Parameter                              | Value                                  | 
| -------------------------------------- | -------------------------------------- | 
| URI                                    | `/user/sessions/{sessionId}/refresh`   | 
| Method                                 | POST                                   | 

#### Headers

##### Cookie

{sessionName}={sessionID}

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

##### X-CSRF-Token

The {csrfToken} needed on all unsafe http methods with session.

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | string      | 
| Default     | n/a         | 
| Required    | no          | 
| Example     | n/a         | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.Session+xml

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Session     | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Session href="user/sessions/go327ij2cirpo59pb6rrv2a4el2/refresh" media-type="application/vnd.ez.api.Session+xml">
  <name>eZSSID</name>
  <identifier>go327ij2cirpo59pb6rrv2a4el2</identifier>
  <csrfToken>23lkneri34ijajedfw39orj3j93</csrfToken>
  <User href="/user/users/14" media-type="vnd.ez.api.User+xml"/>
</Session>
```

##### application/vnd.ez.api.Session+json

| Parameter   | Value       | 
| ----------- | ----------- | 
| Type        | Session     | 

```json
{
  "Session": {
    "name": "eZSSID",
    "identifier": "go327ij2cirpo59pb6rrv2a4el2",
    "csrfToken": "23lkneri34ijajedfw39orj3j93",
    "User": {
      "_href": "/user/users/14",
      "_media-type": "application/vnd.ez.api.User+json"
    }
  }
}
```

##### 404

Error - the session does not exist

## Services

### Countries list

Countries list is a REST service that gives access to an ISO-3166 formatted list of world countries. It is useful when presenting a country options list from any application.

| Parameter               | Value                   | 
| ----------------------- | ----------------------- | 
| URI                     | `/services/countries`   | 
| Method                  | GET                     | 

#### Headers

##### Accept

If set the country list is returned in XML or JSON format

| Parameter                                                                                       | Value                                                                                           | 
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | 
| Type                                                                                            | string                                                                                          | 
| Default                                                                                         | n/a                                                                                             | 
| Required                                                                                        | no                                                                                              | 
| Example                                                                                         | `application/vnd.ez.api.CountriesLis+xml`<br>`application/vnd.ez.api.CountriesLis+json`<br>``   | 

#### Responses

##### 200

###### Payload

##### application/vnd.ez.api.CountriesList+xml

| Parameter     | Value         | 
| ------------- | ------------- | 
| Type          | CountryList   | 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<CountryList media-type="application/vnd.ez.api.CountryList+xml">
    <Country media-type="application/vnd.ez.api.Country+xml" id="AF">
        <name>Afghanistan</name>
        <Alpha2>AF</Alpha2>
        <Alpha3>AFG</Alpha3>
        <IDC>93</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AX">
        <name>Åland</name>
        <Alpha2>AX</Alpha2>
        <Alpha3>ALA</Alpha3>
        <IDC>358</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AL">
        <name>Albania</name>
        <Alpha2>AL</Alpha2>
        <Alpha3>ALB</Alpha3>
        <IDC>355</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="DZ">
        <name>Algeria</name>
        <Alpha2>DZ</Alpha2>
        <Alpha3>DZA</Alpha3>
        <IDC>213</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AS">
        <name>American Samoa</name>
        <Alpha2>AS</Alpha2>
        <Alpha3>ASM</Alpha3>
        <IDC>1684</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AD">
        <name>Andorra</name>
        <Alpha2>AD</Alpha2>
        <Alpha3>AND</Alpha3>
        <IDC>376</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AO">
        <name>Angola</name>
        <Alpha2>AO</Alpha2>
        <Alpha3>AGO</Alpha3>
        <IDC>244</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AI">
        <name>Anguilla</name>
        <Alpha2>AI</Alpha2>
        <Alpha3>AIA</Alpha3>
        <IDC>1264</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AQ">
        <name>Antarctica</name>
        <Alpha2>AQ</Alpha2>
        <Alpha3>ATA</Alpha3>
        <IDC>672</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AG">
        <name>Antigua and Barbuda</name>
        <Alpha2>AG</Alpha2>
        <Alpha3>ATG</Alpha3>
        <IDC>1268</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AR">
        <name>Argentina</name>
        <Alpha2>AR</Alpha2>
        <Alpha3>ARG</Alpha3>
        <IDC>54</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AM">
        <name>Armenia</name>
        <Alpha2>AM</Alpha2>
        <Alpha3>ARM</Alpha3>
        <IDC>374</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AW">
        <name>Aruba</name>
        <Alpha2>AW</Alpha2>
        <Alpha3>ABW</Alpha3>
        <IDC>297</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AU">
        <name>Australia</name>
        <Alpha2>AU</Alpha2>
        <Alpha3>AUS</Alpha3>
        <IDC>61</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AT">
        <name>Austria</name>
        <Alpha2>AT</Alpha2>
        <Alpha3>AUT</Alpha3>
        <IDC>43</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AZ">
        <name>Azerbaijan</name>
        <Alpha2>AZ</Alpha2>
        <Alpha3>AZE</Alpha3>
        <IDC>994</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BS">
        <name>Bahamas</name>
        <Alpha2>BS</Alpha2>
        <Alpha3>BHS</Alpha3>
        <IDC>1242</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BH">
        <name>Bahrain</name>
        <Alpha2>BH</Alpha2>
        <Alpha3>BHR</Alpha3>
        <IDC>973</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BD">
        <name>Bangladesh</name>
        <Alpha2>BD</Alpha2>
        <Alpha3>BGD</Alpha3>
        <IDC>880</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BB">
        <name>Barbados</name>
        <Alpha2>BB</Alpha2>
        <Alpha3>BRB</Alpha3>
        <IDC>1246</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BY">
        <name>Belarus</name>
        <Alpha2>BY</Alpha2>
        <Alpha3>BLR</Alpha3>
        <IDC>375</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BE">
        <name>Belgium</name>
        <Alpha2>BE</Alpha2>
        <Alpha3>BEL</Alpha3>
        <IDC>32</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BZ">
        <name>Belize</name>
        <Alpha2>BZ</Alpha2>
        <Alpha3>BLZ</Alpha3>
        <IDC>501</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BJ">
        <name>Benin</name>
        <Alpha2>BJ</Alpha2>
        <Alpha3>BEN</Alpha3>
        <IDC>229</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BM">
        <name>Bermuda</name>
        <Alpha2>BM</Alpha2>
        <Alpha3>BMU</Alpha3>
        <IDC>1441</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BT">
        <name>Bhutan</name>
        <Alpha2>BT</Alpha2>
        <Alpha3>BTN</Alpha3>
        <IDC>975</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BO">
        <name>Bolivia</name>
        <Alpha2>BO</Alpha2>
        <Alpha3>BOL</Alpha3>
        <IDC>591</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BA">
        <name>Bosnia and Herzegovina</name>
        <Alpha2>BA</Alpha2>
        <Alpha3>BIH</Alpha3>
        <IDC>387</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BW">
        <name>Botswana</name>
        <Alpha2>BW</Alpha2>
        <Alpha3>BWA</Alpha3>
        <IDC>267</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BV">
        <name>Bouvet Island</name>
        <Alpha2>BV</Alpha2>
        <Alpha3>BVT</Alpha3>
        <IDC>47</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BR">
        <name>Brazil</name>
        <Alpha2>BR</Alpha2>
        <Alpha3>BRA</Alpha3>
        <IDC>55</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IO">
        <name>British Indian Ocean Territory</name>
        <Alpha2>IO</Alpha2>
        <Alpha3>IOT</Alpha3>
        <IDC>246</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BN">
        <name>Brunei Darussalam</name>
        <Alpha2>BN</Alpha2>
        <Alpha3>BRN</Alpha3>
        <IDC>673</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BG">
        <name>Bulgaria</name>
        <Alpha2>BG</Alpha2>
        <Alpha3>BGR</Alpha3>
        <IDC>359</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BF">
        <name>Burkina Faso</name>
        <Alpha2>BF</Alpha2>
        <Alpha3>BFA</Alpha3>
        <IDC>226</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BI">
        <name>Burundi</name>
        <Alpha2>BI</Alpha2>
        <Alpha3>BDI</Alpha3>
        <IDC>257</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KH">
        <name>Cambodia</name>
        <Alpha2>KH</Alpha2>
        <Alpha3>KHM</Alpha3>
        <IDC>855</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CM">
        <name>Cameroon</name>
        <Alpha2>CM</Alpha2>
        <Alpha3>CMR</Alpha3>
        <IDC>237</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CA">
        <name>Canada</name>
        <Alpha2>CA</Alpha2>
        <Alpha3>CAN</Alpha3>
        <IDC>1</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CV">
        <name>Cape Verde</name>
        <Alpha2>CV</Alpha2>
        <Alpha3>CPV</Alpha3>
        <IDC>238</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KY">
        <name>Cayman Islands</name>
        <Alpha2>KY</Alpha2>
        <Alpha3>CYM</Alpha3>
        <IDC>1345</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CF">
        <name>Central African Republic</name>
        <Alpha2>CF</Alpha2>
        <Alpha3>CAF</Alpha3>
        <IDC>236</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TD">
        <name>Chad</name>
        <Alpha2>TD</Alpha2>
        <Alpha3>TCD</Alpha3>
        <IDC>235</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CL">
        <name>Chile</name>
        <Alpha2>CL</Alpha2>
        <Alpha3>CHL</Alpha3>
        <IDC>56</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CN">
        <name>China</name>
        <Alpha2>CN</Alpha2>
        <Alpha3>CHN</Alpha3>
        <IDC>86</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CX">
        <name>Christmas Island</name>
        <Alpha2>CX</Alpha2>
        <Alpha3>CXR</Alpha3>
        <IDC>61</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CC">
        <name>Cocos (Keeling) Islands</name>
        <Alpha2>CC</Alpha2>
        <Alpha3>CCK</Alpha3>
        <IDC>61</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CO">
        <name>Colombia</name>
        <Alpha2>CO</Alpha2>
        <Alpha3>COL</Alpha3>
        <IDC>57</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KM">
        <name>Comoros</name>
        <Alpha2>KM</Alpha2>
        <Alpha3>COM</Alpha3>
        <IDC>269</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CG">
        <name>Congo</name>
        <Alpha2>CG</Alpha2>
        <Alpha3>COG</Alpha3>
        <IDC>242</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CD">
        <name>Congo, The Democratic Republic Of The</name>
        <Alpha2>CD</Alpha2>
        <Alpha3>COD</Alpha3>
        <IDC>243</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CK">
        <name>Cook Islands</name>
        <Alpha2>CK</Alpha2>
        <Alpha3>COK</Alpha3>
        <IDC>682</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CR">
        <name>Costa Rica</name>
        <Alpha2>CR</Alpha2>
        <Alpha3>CRI</Alpha3>
        <IDC>506</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CI">
        <name>Côte d'Ivoire</name>
        <Alpha2>CI</Alpha2>
        <Alpha3>CIV</Alpha3>
        <IDC>225</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="HR">
        <name>Croatia</name>
        <Alpha2>HR</Alpha2>
        <Alpha3>HRV</Alpha3>
        <IDC>385</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CU">
        <name>Cuba</name>
        <Alpha2>CU</Alpha2>
        <Alpha3>CUB</Alpha3>
        <IDC>53</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CY">
        <name>Cyprus</name>
        <Alpha2>CY</Alpha2>
        <Alpha3>CYP</Alpha3>
        <IDC>357</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CZ">
        <name>Czech Republic</name>
        <Alpha2>CZ</Alpha2>
        <Alpha3>CZE</Alpha3>
        <IDC>420</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="DK">
        <name>Denmark</name>
        <Alpha2>DK</Alpha2>
        <Alpha3>DNK</Alpha3>
        <IDC>45</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="DJ">
        <name>Djibouti</name>
        <Alpha2>DJ</Alpha2>
        <Alpha3>DJI</Alpha3>
        <IDC>253</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="DM">
        <name>Dominica</name>
        <Alpha2>DM</Alpha2>
        <Alpha3>DMA</Alpha3>
        <IDC>1767</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="DO">
        <name>Dominican Republic</name>
        <Alpha2>DO</Alpha2>
        <Alpha3>DOM</Alpha3>
        <IDC>1809</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="EC">
        <name>Ecuador</name>
        <Alpha2>EC</Alpha2>
        <Alpha3>ECU</Alpha3>
        <IDC>593</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="EG">
        <name>Egypt</name>
        <Alpha2>EG</Alpha2>
        <Alpha3>EGY</Alpha3>
        <IDC>20</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SV">
        <name>El Salvador</name>
        <Alpha2>SV</Alpha2>
        <Alpha3>SLV</Alpha3>
        <IDC>503</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GQ">
        <name>Equatorial Guinea</name>
        <Alpha2>GQ</Alpha2>
        <Alpha3>GNQ</Alpha3>
        <IDC>240</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ER">
        <name>Eritrea</name>
        <Alpha2>ER</Alpha2>
        <Alpha3>ERI</Alpha3>
        <IDC>291</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="EE">
        <name>Estonia</name>
        <Alpha2>EE</Alpha2>
        <Alpha3>EST</Alpha3>
        <IDC>372</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ET">
        <name>Ethiopia</name>
        <Alpha2>ET</Alpha2>
        <Alpha3>ETH</Alpha3>
        <IDC>251</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="FK">
        <name>Falkland Islands (Malvinas)</name>
        <Alpha2>FK</Alpha2>
        <Alpha3>FLK</Alpha3>
        <IDC>500</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="FO">
        <name>Faroe Islands</name>
        <Alpha2>FO</Alpha2>
        <Alpha3>FRO</Alpha3>
        <IDC>298</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="FJ">
        <name>Fiji</name>
        <Alpha2>FJ</Alpha2>
        <Alpha3>FJI</Alpha3>
        <IDC>679</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="FI">
        <name>Finland</name>
        <Alpha2>FI</Alpha2>
        <Alpha3>FIN</Alpha3>
        <IDC>358</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="FR">
        <name>France</name>
        <Alpha2>FR</Alpha2>
        <Alpha3>FRA</Alpha3>
        <IDC>33</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GF">
        <name>French Guiana</name>
        <Alpha2>GF</Alpha2>
        <Alpha3>GUF</Alpha3>
        <IDC>594</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PF">
        <name>French Polynesia</name>
        <Alpha2>PF</Alpha2>
        <Alpha3>PYF</Alpha3>
        <IDC>689</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TF">
        <name>French Southern Territories</name>
        <Alpha2>TF</Alpha2>
        <Alpha3>ATF</Alpha3>
        <IDC>0</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GA">
        <name>Gabon</name>
        <Alpha2>GA</Alpha2>
        <Alpha3>GAB</Alpha3>
        <IDC>241</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GM">
        <name>Gambia</name>
        <Alpha2>GM</Alpha2>
        <Alpha3>GMB</Alpha3>
        <IDC>220</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GE">
        <name>Georgia</name>
        <Alpha2>GE</Alpha2>
        <Alpha3>GEO</Alpha3>
        <IDC>995</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="DE">
        <name>Germany</name>
        <Alpha2>DE</Alpha2>
        <Alpha3>DEU</Alpha3>
        <IDC>49</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GH">
        <name>Ghana</name>
        <Alpha2>GH</Alpha2>
        <Alpha3>GHA</Alpha3>
        <IDC>233</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GI">
        <name>Gibraltar</name>
        <Alpha2>GI</Alpha2>
        <Alpha3>GIB</Alpha3>
        <IDC>350</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GR">
        <name>Greece</name>
        <Alpha2>GR</Alpha2>
        <Alpha3>GRC</Alpha3>
        <IDC>30</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GL">
        <name>Greenland</name>
        <Alpha2>GL</Alpha2>
        <Alpha3>GRL</Alpha3>
        <IDC>299</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GD">
        <name>Grenada</name>
        <Alpha2>GD</Alpha2>
        <Alpha3>GRD</Alpha3>
        <IDC>1473</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GP">
        <name>Guadeloupe</name>
        <Alpha2>GP</Alpha2>
        <Alpha3>GLP</Alpha3>
        <IDC>590</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GU">
        <name>Guam</name>
        <Alpha2>GU</Alpha2>
        <Alpha3>GUM</Alpha3>
        <IDC>1671</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GT">
        <name>Guatemala</name>
        <Alpha2>GT</Alpha2>
        <Alpha3>GTM</Alpha3>
        <IDC>502</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GG">
        <name>Guernsey</name>
        <Alpha2>GG</Alpha2>
        <Alpha3>GGY</Alpha3>
        <IDC>44</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GN">
        <name>Guinea</name>
        <Alpha2>GN</Alpha2>
        <Alpha3>GIN</Alpha3>
        <IDC>224</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GW">
        <name>Guinea-Bissau</name>
        <Alpha2>GW</Alpha2>
        <Alpha3>GNB</Alpha3>
        <IDC>245</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GY">
        <name>Guyana</name>
        <Alpha2>GY</Alpha2>
        <Alpha3>GUY</Alpha3>
        <IDC>592</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="HT">
        <name>Haiti</name>
        <Alpha2>HT</Alpha2>
        <Alpha3>HTI</Alpha3>
        <IDC>509</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="HM">
        <name>Heard Island and McDonald Islands</name>
        <Alpha2>HM</Alpha2>
        <Alpha3>HMD</Alpha3>
        <IDC>672</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="HN">
        <name>Honduras</name>
        <Alpha2>HN</Alpha2>
        <Alpha3>HND</Alpha3>
        <IDC>504</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="HK">
        <name>Hong Kong</name>
        <Alpha2>HK</Alpha2>
        <Alpha3>HKG</Alpha3>
        <IDC>852</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="HU">
        <name>Hungary</name>
        <Alpha2>HU</Alpha2>
        <Alpha3>HUN</Alpha3>
        <IDC>36</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IS">
        <name>Iceland</name>
        <Alpha2>IS</Alpha2>
        <Alpha3>ISL</Alpha3>
        <IDC>354</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IN">
        <name>India</name>
        <Alpha2>IN</Alpha2>
        <Alpha3>IND</Alpha3>
        <IDC>91</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ID">
        <name>Indonesia</name>
        <Alpha2>ID</Alpha2>
        <Alpha3>IDN</Alpha3>
        <IDC>62</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IR">
        <name>Iran, Islamic Republic of</name>
        <Alpha2>IR</Alpha2>
        <Alpha3>IRN</Alpha3>
        <IDC>98</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IQ">
        <name>Iraq</name>
        <Alpha2>IQ</Alpha2>
        <Alpha3>IRQ</Alpha3>
        <IDC>964</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IE">
        <name>Ireland</name>
        <Alpha2>IE</Alpha2>
        <Alpha3>IRL</Alpha3>
        <IDC>353</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IM">
        <name>Isle of Man</name>
        <Alpha2>IM</Alpha2>
        <Alpha3>IMN</Alpha3>
        <IDC>44</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IL">
        <name>Israel</name>
        <Alpha2>IL</Alpha2>
        <Alpha3>ISR</Alpha3>
        <IDC>972</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="IT">
        <name>Italy</name>
        <Alpha2>IT</Alpha2>
        <Alpha3>ITA</Alpha3>
        <IDC>39</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="JM">
        <name>Jamaica</name>
        <Alpha2>JM</Alpha2>
        <Alpha3>JAM</Alpha3>
        <IDC>1876</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="JP">
        <name>Japan</name>
        <Alpha2>JP</Alpha2>
        <Alpha3>JPN</Alpha3>
        <IDC>81</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="JE">
        <name>Jersey</name>
        <Alpha2>JE</Alpha2>
        <Alpha3>JEY</Alpha3>
        <IDC>44</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="JO">
        <name>Jordan</name>
        <Alpha2>JO</Alpha2>
        <Alpha3>JOR</Alpha3>
        <IDC>962</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KZ">
        <name>Kazakhstan</name>
        <Alpha2>KZ</Alpha2>
        <Alpha3>KAZ</Alpha3>
        <IDC>7</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KE">
        <name>Kenya</name>
        <Alpha2>KE</Alpha2>
        <Alpha3>KEN</Alpha3>
        <IDC>254</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KI">
        <name>Kiribati</name>
        <Alpha2>KI</Alpha2>
        <Alpha3>KIR</Alpha3>
        <IDC>686</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KP">
        <name>Korea, Democratic People's Republic of</name>
        <Alpha2>KP</Alpha2>
        <Alpha3>PRK</Alpha3>
        <IDC>850</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KR">
        <name>Korea, Republic of</name>
        <Alpha2>KR</Alpha2>
        <Alpha3>KOR</Alpha3>
        <IDC>82</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KW">
        <name>Kuwait</name>
        <Alpha2>KW</Alpha2>
        <Alpha3>KWT</Alpha3>
        <IDC>965</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KG">
        <name>Kyrgyzstan</name>
        <Alpha2>KG</Alpha2>
        <Alpha3>KGZ</Alpha3>
        <IDC>996</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LA">
        <name>Lao People's Democratic Republic</name>
        <Alpha2>LA</Alpha2>
        <Alpha3>LAO</Alpha3>
        <IDC>856</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LV">
        <name>Latvia</name>
        <Alpha2>LV</Alpha2>
        <Alpha3>LVA</Alpha3>
        <IDC>371</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LB">
        <name>Lebanon</name>
        <Alpha2>LB</Alpha2>
        <Alpha3>LBN</Alpha3>
        <IDC>961</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LS">
        <name>Lesotho</name>
        <Alpha2>LS</Alpha2>
        <Alpha3>LSO</Alpha3>
        <IDC>266</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LR">
        <name>Liberia</name>
        <Alpha2>LR</Alpha2>
        <Alpha3>LBR</Alpha3>
        <IDC>231</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LY">
        <name>Libyan Arab Jamahiriya</name>
        <Alpha2>LY</Alpha2>
        <Alpha3>LBY</Alpha3>
        <IDC>218</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LI">
        <name>Liechtenstein</name>
        <Alpha2>LI</Alpha2>
        <Alpha3>LIE</Alpha3>
        <IDC>423</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LT">
        <name>Lithuania</name>
        <Alpha2>LT</Alpha2>
        <Alpha3>LTU</Alpha3>
        <IDC>370</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LU">
        <name>Luxembourg</name>
        <Alpha2>LU</Alpha2>
        <Alpha3>LUX</Alpha3>
        <IDC>352</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MO">
        <name>Macau</name>
        <Alpha2>MO</Alpha2>
        <Alpha3>MAC</Alpha3>
        <IDC>853</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MK">
        <name>Macedonia, The Former Yugoslav Republic of</name>
        <Alpha2>MK</Alpha2>
        <Alpha3>MKD</Alpha3>
        <IDC>389</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MG">
        <name>Madagascar</name>
        <Alpha2>MG</Alpha2>
        <Alpha3>MDG</Alpha3>
        <IDC>261</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MW">
        <name>Malawi</name>
        <Alpha2>MW</Alpha2>
        <Alpha3>MWI</Alpha3>
        <IDC>265</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MY">
        <name>Malaysia</name>
        <Alpha2>MY</Alpha2>
        <Alpha3>MYS</Alpha3>
        <IDC>60</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MV">
        <name>Maldives</name>
        <Alpha2>MV</Alpha2>
        <Alpha3>MDV</Alpha3>
        <IDC>960</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ML">
        <name>Mali</name>
        <Alpha2>ML</Alpha2>
        <Alpha3>MLI</Alpha3>
        <IDC>223</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MT">
        <name>Malta</name>
        <Alpha2>MT</Alpha2>
        <Alpha3>MLT</Alpha3>
        <IDC>356</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MH">
        <name>Marshall Islands</name>
        <Alpha2>MH</Alpha2>
        <Alpha3>MHL</Alpha3>
        <IDC>692</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MQ">
        <name>Martinique</name>
        <Alpha2>MQ</Alpha2>
        <Alpha3>MTQ</Alpha3>
        <IDC>596</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MR">
        <name>Mauritania</name>
        <Alpha2>MR</Alpha2>
        <Alpha3>MRT</Alpha3>
        <IDC>222</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MU">
        <name>Mauritius</name>
        <Alpha2>MU</Alpha2>
        <Alpha3>MUS</Alpha3>
        <IDC>230</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="YT">
        <name>Mayotte</name>
        <Alpha2>YT</Alpha2>
        <Alpha3>MYT</Alpha3>
        <IDC>262</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MX">
        <name>Mexico</name>
        <Alpha2>MX</Alpha2>
        <Alpha3>MEX</Alpha3>
        <IDC>52</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="FM">
        <name>Micronesia, Federated States of</name>
        <Alpha2>FM</Alpha2>
        <Alpha3>FSM</Alpha3>
        <IDC>691</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MD">
        <name>Moldova, Republic of</name>
        <Alpha2>MD</Alpha2>
        <Alpha3>MDA</Alpha3>
        <IDC>373</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MC">
        <name>Monaco</name>
        <Alpha2>MC</Alpha2>
        <Alpha3>MCO</Alpha3>
        <IDC>377</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MN">
        <name>Mongolia</name>
        <Alpha2>MN</Alpha2>
        <Alpha3>MNG</Alpha3>
        <IDC>976</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ME">
        <name>Montenegro</name>
        <Alpha2>ME</Alpha2>
        <Alpha3>MNE</Alpha3>
        <IDC>382</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MS">
        <name>Montserrat</name>
        <Alpha2>MS</Alpha2>
        <Alpha3>MSR</Alpha3>
        <IDC>1664</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MA">
        <name>Morocco</name>
        <Alpha2>MA</Alpha2>
        <Alpha3>MAR</Alpha3>
        <IDC>212</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MZ">
        <name>Mozambique</name>
        <Alpha2>MZ</Alpha2>
        <Alpha3>MOZ</Alpha3>
        <IDC>258</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MM">
        <name>Myanmar</name>
        <Alpha2>MM</Alpha2>
        <Alpha3>MMR</Alpha3>
        <IDC>95</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NA">
        <name>Namibia</name>
        <Alpha2>NA</Alpha2>
        <Alpha3>NAM</Alpha3>
        <IDC>264</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NR">
        <name>Nauru</name>
        <Alpha2>NR</Alpha2>
        <Alpha3>NRU</Alpha3>
        <IDC>674</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NP">
        <name>Nepal</name>
        <Alpha2>NP</Alpha2>
        <Alpha3>NPL</Alpha3>
        <IDC>977</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NL">
        <name>Netherlands</name>
        <Alpha2>NL</Alpha2>
        <Alpha3>NLD</Alpha3>
        <IDC>31</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AN">
        <name>Netherlands Antilles</name>
        <Alpha2>AN</Alpha2>
        <Alpha3>ANT</Alpha3>
        <IDC>599</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NC">
        <name>New Caledonia</name>
        <Alpha2>NC</Alpha2>
        <Alpha3>NCL</Alpha3>
        <IDC>687</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NZ">
        <name>New Zealand</name>
        <Alpha2>NZ</Alpha2>
        <Alpha3>NZL</Alpha3>
        <IDC>64</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NI">
        <name>Nicaragua</name>
        <Alpha2>NI</Alpha2>
        <Alpha3>NIC</Alpha3>
        <IDC>505</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NE">
        <name>Niger</name>
        <Alpha2>NE</Alpha2>
        <Alpha3>NER</Alpha3>
        <IDC>227</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NG">
        <name>Nigeria</name>
        <Alpha2>NG</Alpha2>
        <Alpha3>NGA</Alpha3>
        <IDC>234</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NU">
        <name>Niue</name>
        <Alpha2>NU</Alpha2>
        <Alpha3>NIU</Alpha3>
        <IDC>683</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NF">
        <name>Norfolk Island</name>
        <Alpha2>NF</Alpha2>
        <Alpha3>NFK</Alpha3>
        <IDC>6723</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MP">
        <name>Northern Mariana Islands</name>
        <Alpha2>MP</Alpha2>
        <Alpha3>MNP</Alpha3>
        <IDC>1670</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="NO">
        <name>Norway</name>
        <Alpha2>NO</Alpha2>
        <Alpha3>NOR</Alpha3>
        <IDC>47</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="OM">
        <name>Oman</name>
        <Alpha2>OM</Alpha2>
        <Alpha3>OMN</Alpha3>
        <IDC>968</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PK">
        <name>Pakistan</name>
        <Alpha2>PK</Alpha2>
        <Alpha3>PAK</Alpha3>
        <IDC>92</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PW">
        <name>Palau</name>
        <Alpha2>PW</Alpha2>
        <Alpha3>PLW</Alpha3>
        <IDC>680</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PS">
        <name>Palestinian Territory, Occupied</name>
        <Alpha2>PS</Alpha2>
        <Alpha3>PSE</Alpha3>
        <IDC>970</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PA">
        <name>Panama</name>
        <Alpha2>PA</Alpha2>
        <Alpha3>PAN</Alpha3>
        <IDC>507</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PG">
        <name>Papua New Guinea</name>
        <Alpha2>PG</Alpha2>
        <Alpha3>PNG</Alpha3>
        <IDC>675</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PY">
        <name>Paraguay</name>
        <Alpha2>PY</Alpha2>
        <Alpha3>PRY</Alpha3>
        <IDC>595</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PE">
        <name>Peru</name>
        <Alpha2>PE</Alpha2>
        <Alpha3>PER</Alpha3>
        <IDC>51</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PH">
        <name>Philippines</name>
        <Alpha2>PH</Alpha2>
        <Alpha3>PHL</Alpha3>
        <IDC>63</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PN">
        <name>Pitcairn</name>
        <Alpha2>PN</Alpha2>
        <Alpha3>PCN</Alpha3>
        <IDC>64</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PL">
        <name>Poland</name>
        <Alpha2>PL</Alpha2>
        <Alpha3>POL</Alpha3>
        <IDC>48</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PT">
        <name>Portugal</name>
        <Alpha2>PT</Alpha2>
        <Alpha3>PRT</Alpha3>
        <IDC>351</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PR">
        <name>Puerto Rico</name>
        <Alpha2>PR</Alpha2>
        <Alpha3>PRI</Alpha3>
        <IDC>1787</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="QA">
        <name>Qatar</name>
        <Alpha2>QA</Alpha2>
        <Alpha3>QAT</Alpha3>
        <IDC>974</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="RE">
        <name>Reunion</name>
        <Alpha2>RE</Alpha2>
        <Alpha3>REU</Alpha3>
        <IDC>262</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="RO">
        <name>Romania</name>
        <Alpha2>RO</Alpha2>
        <Alpha3>ROU</Alpha3>
        <IDC>40</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="RU">
        <name>Russian Federation</name>
        <Alpha2>RU</Alpha2>
        <Alpha3>RUS</Alpha3>
        <IDC>7</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="RW">
        <name>Rwanda</name>
        <Alpha2>RW</Alpha2>
        <Alpha3>RWA</Alpha3>
        <IDC>250</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="BL">
        <name>Saint Barthélemy</name>
        <Alpha2>BL</Alpha2>
        <Alpha3>BLM</Alpha3>
        <IDC>590</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SH">
        <name>Saint Helena</name>
        <Alpha2>SH</Alpha2>
        <Alpha3>SHN</Alpha3>
        <IDC>290</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="KN">
        <name>Saint Kitts and Nevis</name>
        <Alpha2>KN</Alpha2>
        <Alpha3>KNA</Alpha3>
        <IDC>1869</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LC">
        <name>Saint Lucia</name>
        <Alpha2>LC</Alpha2>
        <Alpha3>LCA</Alpha3>
        <IDC>1758</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="MF">
        <name>Saint Martin</name>
        <Alpha2>MF</Alpha2>
        <Alpha3>MAF</Alpha3>
        <IDC>590</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="PM">
        <name>Saint Pierre and Miquelon</name>
        <Alpha2>PM</Alpha2>
        <Alpha3>SPM</Alpha3>
        <IDC>508</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VC">
        <name>Saint Vincent and The Grenadines</name>
        <Alpha2>VC</Alpha2>
        <Alpha3>VCT</Alpha3>
        <IDC>1784</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="WS">
        <name>Samoa</name>
        <Alpha2>WS</Alpha2>
        <Alpha3>WSM</Alpha3>
        <IDC>685</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SM">
        <name>San Marino</name>
        <Alpha2>SM</Alpha2>
        <Alpha3>SMR</Alpha3>
        <IDC>378</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ST">
        <name>Sao Tome and Principe</name>
        <Alpha2>ST</Alpha2>
        <Alpha3>STP</Alpha3>
        <IDC>239</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SA">
        <name>Saudi Arabia</name>
        <Alpha2>SA</Alpha2>
        <Alpha3>SAU</Alpha3>
        <IDC>966</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SN">
        <name>Senegal</name>
        <Alpha2>SN</Alpha2>
        <Alpha3>SEN</Alpha3>
        <IDC>221</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="RS">
        <name>Serbia</name>
        <Alpha2>RS</Alpha2>
        <Alpha3>SRB</Alpha3>
        <IDC>381</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SC">
        <name>Seychelles</name>
        <Alpha2>SC</Alpha2>
        <Alpha3>SYC</Alpha3>
        <IDC>248</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SL">
        <name>Sierra Leone</name>
        <Alpha2>SL</Alpha2>
        <Alpha3>SLE</Alpha3>
        <IDC>232</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SG">
        <name>Singapore</name>
        <Alpha2>SG</Alpha2>
        <Alpha3>SGP</Alpha3>
        <IDC>65</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SK">
        <name>Slovakia</name>
        <Alpha2>SK</Alpha2>
        <Alpha3>SVK</Alpha3>
        <IDC>421</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SI">
        <name>Slovenia</name>
        <Alpha2>SI</Alpha2>
        <Alpha3>SVN</Alpha3>
        <IDC>386</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SB">
        <name>Solomon Islands</name>
        <Alpha2>SB</Alpha2>
        <Alpha3>SLB</Alpha3>
        <IDC>677</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SO">
        <name>Somalia</name>
        <Alpha2>SO</Alpha2>
        <Alpha3>SOM</Alpha3>
        <IDC>252</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ZA">
        <name>South Africa</name>
        <Alpha2>ZA</Alpha2>
        <Alpha3>ZAF</Alpha3>
        <IDC>27</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GS">
        <name>South Georgia and The South Sandwich Islands</name>
        <Alpha2>GS</Alpha2>
        <Alpha3>SGS</Alpha3>
        <IDC>500</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ES">
        <name>Spain</name>
        <Alpha2>ES</Alpha2>
        <Alpha3>ESP</Alpha3>
        <IDC>34</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="LK">
        <name>Sri Lanka</name>
        <Alpha2>LK</Alpha2>
        <Alpha3>LKA</Alpha3>
        <IDC>94</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SD">
        <name>Sudan</name>
        <Alpha2>SD</Alpha2>
        <Alpha3>SDN</Alpha3>
        <IDC>249</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SR">
        <name>Suriname</name>
        <Alpha2>SR</Alpha2>
        <Alpha3>SUR</Alpha3>
        <IDC>597</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SJ">
        <name>Svalbard and Jan Mayen</name>
        <Alpha2>SJ</Alpha2>
        <Alpha3>SJM</Alpha3>
        <IDC>47</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SZ">
        <name>Swaziland</name>
        <Alpha2>SZ</Alpha2>
        <Alpha3>SWZ</Alpha3>
        <IDC>268</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SE">
        <name>Sweden</name>
        <Alpha2>SE</Alpha2>
        <Alpha3>SWE</Alpha3>
        <IDC>46</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="CH">
        <name>Switzerland</name>
        <Alpha2>CH</Alpha2>
        <Alpha3>CHE</Alpha3>
        <IDC>41</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="SY">
        <name>Syrian Arab Republic</name>
        <Alpha2>SY</Alpha2>
        <Alpha3>SYR</Alpha3>
        <IDC>963</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TW">
        <name>Taiwan</name>
        <Alpha2>TW</Alpha2>
        <Alpha3>TWN</Alpha3>
        <IDC>886</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TJ">
        <name>Tajikistan</name>
        <Alpha2>TJ</Alpha2>
        <Alpha3>TJK</Alpha3>
        <IDC>992</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TZ">
        <name>Tanzania, United Republic of</name>
        <Alpha2>TZ</Alpha2>
        <Alpha3>TZA</Alpha3>
        <IDC>255</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TH">
        <name>Thailand</name>
        <Alpha2>TH</Alpha2>
        <Alpha3>THA</Alpha3>
        <IDC>66</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TL">
        <name>Timor-Leste</name>
        <Alpha2>TL</Alpha2>
        <Alpha3>TLS</Alpha3>
        <IDC>670</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TG">
        <name>Togo</name>
        <Alpha2>TG</Alpha2>
        <Alpha3>TGO</Alpha3>
        <IDC>228</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TK">
        <name>Tokelau</name>
        <Alpha2>TK</Alpha2>
        <Alpha3>TKL</Alpha3>
        <IDC>690</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TO">
        <name>Tonga</name>
        <Alpha2>TO</Alpha2>
        <Alpha3>TON</Alpha3>
        <IDC>676</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TT">
        <name>Trinidad and Tobago</name>
        <Alpha2>TT</Alpha2>
        <Alpha3>TTO</Alpha3>
        <IDC>1868</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TN">
        <name>Tunisia</name>
        <Alpha2>TN</Alpha2>
        <Alpha3>TUN</Alpha3>
        <IDC>216</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TR">
        <name>Turkey</name>
        <Alpha2>TR</Alpha2>
        <Alpha3>TUR</Alpha3>
        <IDC>90</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TM">
        <name>Turkmenistan</name>
        <Alpha2>TM</Alpha2>
        <Alpha3>TKM</Alpha3>
        <IDC>993</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TC">
        <name>Turks and Caicos Islands</name>
        <Alpha2>TC</Alpha2>
        <Alpha3>TCA</Alpha3>
        <IDC>1649</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="TV">
        <name>Tuvalu</name>
        <Alpha2>TV</Alpha2>
        <Alpha3>TUV</Alpha3>
        <IDC>688</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="UG">
        <name>Uganda</name>
        <Alpha2>UG</Alpha2>
        <Alpha3>UGA</Alpha3>
        <IDC>256</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="UA">
        <name>Ukraine</name>
        <Alpha2>UA</Alpha2>
        <Alpha3>UKR</Alpha3>
        <IDC>380</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="AE">
        <name>United Arab Emirates</name>
        <Alpha2>AE</Alpha2>
        <Alpha3>ARE</Alpha3>
        <IDC>971</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="GB">
        <name>United Kingdom</name>
        <Alpha2>GB</Alpha2>
        <Alpha3>GBR</Alpha3>
        <IDC>44</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="UM">
        <name>United States Minor Outlying Islands</name>
        <Alpha2>UM</Alpha2>
        <Alpha3>UMI</Alpha3>
        <IDC>1</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="US">
        <name>United States of America</name>
        <Alpha2>US</Alpha2>
        <Alpha3>USA</Alpha3>
        <IDC>1</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="UY">
        <name>Uruguay</name>
        <Alpha2>UY</Alpha2>
        <Alpha3>URY</Alpha3>
        <IDC>598</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="UZ">
        <name>Uzbekistan</name>
        <Alpha2>UZ</Alpha2>
        <Alpha3>UZB</Alpha3>
        <IDC>998</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VU">
        <name>Vanuatu</name>
        <Alpha2>VU</Alpha2>
        <Alpha3>VUT</Alpha3>
        <IDC>678</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VA">
        <name>Holy See (Vatican City State)</name>
        <Alpha2>VA</Alpha2>
        <Alpha3>VAT</Alpha3>
        <IDC>3906</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VE">
        <name>Venezuela</name>
        <Alpha2>VE</Alpha2>
        <Alpha3>VEN</Alpha3>
        <IDC>58</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VN">
        <name>Viet Nam</name>
        <Alpha2>VN</Alpha2>
        <Alpha3>VNM</Alpha3>
        <IDC>84</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VG">
        <name>Virgin Islands, British</name>
        <Alpha2>VG</Alpha2>
        <Alpha3>VGB</Alpha3>
        <IDC>1284</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="VI">
        <name>Virgin Islands, U.S.</name>
        <Alpha2>VI</Alpha2>
        <Alpha3>VIR</Alpha3>
        <IDC>1340</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="WF">
        <name>Wallis and Futuna</name>
        <Alpha2>WF</Alpha2>
        <Alpha3>WLF</Alpha3>
        <IDC>681</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="EH">
        <name>Western Sahara</name>
        <Alpha2>EH</Alpha2>
        <Alpha3>ESH</Alpha3>
        <IDC>212</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="YE">
        <name>Yemen</name>
        <Alpha2>YE</Alpha2>
        <Alpha3>YEM</Alpha3>
        <IDC>967</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ZM">
        <name>Zambia</name>
        <Alpha2>ZM</Alpha2>
        <Alpha3>ZMB</Alpha3>
        <IDC>260</IDC>
    </Country>
    <Country media-type="application/vnd.ez.api.Country+xml" id="ZW">
        <name>Zimbabwe</name>
        <Alpha2>ZW</Alpha2>
        <Alpha3>ZWE</Alpha3>
        <IDC>263</IDC>
    </Country>
</CountryList>
```

