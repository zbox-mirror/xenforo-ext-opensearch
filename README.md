# Information

| Property     | Value                                              |
| ------------ | -------------------------------------------------- |
| ID           | `ext_167e279a`                                     |
| Type         | Add-on                                             |
| License      | MIT                                                |
| Language     | Russian                                            |
| Requirements | XenForo 2.1                                        |
| Authors      | [z17 Dev](mailto:mail@z17.dev)                     |

Набор технологий, позволяющих веб-сайтам и поисковым системам публиковать результаты поиска в форматах, удобных для распространения и сбора.

## Install

1. [Загрузить](https://github.com/zmarket/xenforo-ext-opensearch/tags) архив с последней версией расширения.
2. Распаковать содержимое архива в `/src/addons/CMFStore/ext_167e279a/`, сохраняя структуру директорий.
3. Зайти в **AdminCP**, далее *Add-ons*, и установить необходимое расширение.
4. Создать файл `ext.opensearch.xml` в корне форума со следующим содержимым:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/"
                       xmlns:moz="http://www.mozilla.org/2006/browser/search/">
    <ShortName>Web Search</ShortName>
    <Description>Use XenForo.com to search the Web.</Description>
    <Tags>sci-fi forums fantasy horror</Tags>
    <Contact>support@xenforo.com</Contact>
    <Url type="text/html" method="get"
         template="https://xenforo.com/search/search?keywords={searchTerms}"/>
    <Url type="application/opensearchdescription+xml" rel="self"
         template="https://xenforo.com/ext.opensearch.xml"/>
    <LongName>Cool XenForo Community</LongName>
    <Image height="64" width="64" type="image/png">https://xenforo.com/websearch.png</Image>
    <Image height="16" width="16" type="image/x-icon">https://xenforo.com/favicon.ico</Image>
    <Developer>XenForo.com Development Team</Developer>
    <Attribution>
        Search data Copyright 2005, XenForo.com, Inc., All Rights Reserved
    </Attribution>
    <SyndicationRight>open</SyndicationRight>
    <AdultContent>false</AdultContent>
    <Language>*</Language>
    <OutputEncoding>UTF-8</OutputEncoding>
    <InputEncoding>UTF-8</InputEncoding>
    <moz:SearchForm>https://xenforo.com/search/</moz:SearchForm>
</OpenSearchDescription>
```

## Update

1. [Загрузить](https://github.com/zmarket/xenforo-ext-opensearch/tags) архив с новой версией расширения.
2. Распаковать содержимое архива в `/src/addons/CMFStore/ext_167e279a/`, сохраняя структуру директорий, заменяя существующие файлы и папки.
3. Зайти в **AdminCP**, далее *Add-ons*, и обновить необходимое расширение.
