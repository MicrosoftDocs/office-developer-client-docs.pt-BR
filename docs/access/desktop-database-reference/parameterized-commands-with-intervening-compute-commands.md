---
title: Comandos parametrizados com comandos COMPUTE intermediários
TOCTitle: Parameterized commands with intervening COMPUTE commands
ms:assetid: ff3724cd-040b-4b5f-bb9b-e6a38fd938c9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250311(v=office.15)
ms:contentKeyID: 48548959
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4172fba2d9fc08d3cf9f588fe9ace65da7997b19
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701932"
---
# <a name="parameterized-commands-with-intervening-compute-commands"></a>Comandos parametrizados com comandos COMPUTE intermediários


**Aplica-se a**: Access 2013, o Office 2013

Um comando APPEND de forma parametrizada comum tem uma cláusula que cria um **Recordset** pai com um comando query e outra cláusula que cria um **Recordset** filho com um comando query parametrizado  ou seja, um comando que contém um marcador de parâmetro (um ponto de interrogação, "?"). A forma resultante do **Recordset** tem dois níveis, nos quais o pai ocupa o nível superior e o filho ocupa o nível inferior.

A cláusula que cria o **Recordset** filho agora pode ser um número arbitrário de comandos COMPUTE de forma aninhada, nos quais o comando aninhado mais profundamente contém a consulta parametrizada. A forma resultante do **Recordset** tem dois níveis, nos quais o pai ocupa o nível mais superior, o filho ocupa o nível mais inferior e um número arbitrário de **Recordset**s gerados pelos comandos COMPUTE de forma ocupam os níveis intermediários.

O uso típico deste recurso é chamar a função de agregação e agrupar as capacidades dos comandos COMPUTE de forma para criar objetos **Recordset** intermediários com informações analíticas sobre o **Recordset** filho. Além do mais, como este é um comando shape parametrizado, cada vez que uma coluna de capítulo do pai é acessada, um novo **Recordset** filho pode ser recuperado. Uma vez que os níveis intermediários são derivados do filho, eles também serão recalculados.

