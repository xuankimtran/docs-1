---
title: "Command Compatibility between Selenium IDE and KR" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/side-kr-command-compatibility.html 
description: 
toc: false
---

During the migration process, KR will remove or transform certain Selenium IDE to make the tests functional. The following table contains more details:


| Selenium Command                                | KR  | KR alternative                 |
|-------------------------------------------------|-----|--------------------------------|
| add selection                                   | Yes | addSelection                   |
| answer on next prompt                           | Yes | answerOnNextPrompt             |
| assert                                          | No  |                                |
| assert alert                                    | Yes | assertAlert                    |
| assert checked                                  | Yes | assertChecked                  |
| assert confirmation                             | Yes | assertConfirmation             |
| assert editable                                 | Yes | assertEditable                 |
| assert element present                          | Yes | assertElementPresent           |
| assert element not present                      | Yes | assertElementNotPresent        |
| assert not checked                              | Yes | assertNotChecked               |
| assert not editable                             | Yes | assertNotEditable              |
| assert not selected value                       | Yes | assertNotSelectedValue         |
| assert not text                                 | Yes | assertNotText                  |
| assert prompt                                   | Yes | assertPrompt                   |
| assert selected value                           | Yes | assertSelectedValue            |
| assert selected label                           | Yes | assertSelectedLabel            |
| assert text                                     | Yes | assertText                     |
| assert title                                    | Yes | assertTitle                    |
| assert value                                    | Yes | assertValue                    |
| check                                           | Yes | check                          |
| choose cancel on next confirmation              | Yes | chooseCancelOnNextConfirmation |
| choose cancel on next prompt                    | Yes | chooseCancelOnNextPrompt       |
| choose ok on next confirmation                  | Yes | chooseOkOnNextConfirmation     |
| click                                           | Yes | click                          |
| click at                                        | Yes | clickAt                        |
| close                                           | Yes | close                          |
| debugger                                        | No  |                                |
| do                                              | No  |                                |
| double click                                    | Yes | doubleClick                    |
| double click at                                 | Yes | doubleClickAt                  |
| drag and drop to object                         | Yes | dragAndDropToObject            |
| echo                                            | Yes | echo                           |
| edit content                                    | Yes | editContent                    |
| else                                            | Yes | else                           |
| else if                                         | Yes | elseIf                         |
| end                                             | No  |                                |
| execute script                                  | No  |                                |
| execute async script                            | No  |                                |
| for each                                        | No  |                                |
| if                                              | Yes | if                             |
| mouse down                                      | Yes | mouseDown                      |
| mouse down at                                   | Yes | mouseDownAt                    |
| mouse move at                                   | Yes | mouseMoveAt                    |
| mouse out                                       | Yes | mouseOut                       |
| mouse over                                      | Yes | mouseOver                      |
| mouse up                                        | Yes | mouseUp                        |
| mouse up at                                     | Yes | mouseUpAt                      |
| open                                            | Yes | open                           |
| pause                                           | Yes | pause                          |
| remove selection                                | Yes | removeSelection                |
| repeat if                                       | No  |                                |
| run                                             | No  |                                |
| run script                                      | Yes | runScript                      |
| select                                          | No  | select                         |
| select frame                                    | Yes | selectFrame                    |
| select window                                   | No  |                                |
| Root → win_ser_local"                           |     |                                |
| send keys                                       | Yes | sendKeys                       |
| set speed                                       | Yes | setSpeed                       |
| set window size                                 | No  |                                |
| store                                           | Yes | store                          |
| store attribute                                 | Yes | storeAttribute                 |
| store json                                      | No  |                                |
| store text                                      | Yes | storeText                      |
| store title                                     | Yes | storeTitle                     |
| store value                                     | Yes | storeValue                     |
| store window handle                             | No  |                                |
| store xpath count                               | Yes | storeXpathCount                |
| submit                                          | Yes | submit                         |
| times                                           | No  |                                |
| type                                            | Yes | type                           |
| uncheck                                         | Yes | uncheck                        |
| verify                                          | No  |                                |
| verify checked                                  | Yes | verifyChecked                  |
| verify editable                                 | Yes | verifyEditable                 |
| verify element present                          | Yes | verifyElementPresent           |
| verify element not present                      | Yes | verifyElementNotPresent        |
| verify not checked                              | Yes | verifyNotChecked               |
| verify not editable                             | Yes | verifyNotEditable              |
| verify not selected value                       | Yes | verifyNotSelectedValue         |
| verify not text                                 | Yes | verifyNotText                  |
| verify selected label                           | Yes | verifySelectedLabel            |
| verify selected value                           | Yes | verifySelectedValue            |
| verify text                                     | Yes | verifyText                     |
| verify title                                    | Yes | verifyTitle                    |
| verify value                                    | Yes | verifyValue                    |
| wait for element editable                       | Yes | waitForEditable                |
| wait for element not editable                   | Yes | waitForNotEditable             |
| wait for element not present                    | Yes | waitForElementNotPresent       |
| wait for element not visible                    | Yes | waitForNotVisible              |
| wait for element present                        | Yes | waitForElementPresent          |
| wait for element visible                        | Yes | waitForVisible                 |
| webdriver answer on visible prompt              | No  |                                |
| webdriver choose cancel on visible confirmation | No  |                                |
| webdriver choose cancel on visible prompt       | No  |                                |
| while                                           | Yes |                                |
