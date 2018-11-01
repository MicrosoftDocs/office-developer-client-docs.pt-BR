---
title: O papel do ADO no Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23502ec1bc4ebd0bcdbca17763c2e9dd467d8793
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884517"
---
# <a name="the-role-of-ado-in-microsoft-data-access"></a>O papel do ADO no Microsoft Data Access


**Aplica-se a**: Access 2013, o Office 2013

O Microsoft Data Access Components (MDAC) fornece acesso a dados independente de repositórios de dados, ferramentas e linguagens. Ele fornece uma interface fácil de usar de nível alto e uma interface de nível baixo e alto desempenho para praticamente qualquer repositório de dados disponível. Você pode usar essa flexibilidade para integrar vários repositórios de dados e usar suas opções de ferramentas, aplicativos e serviços de plataforma para criar as soluções certas para suas necessidades. Essa tecnologia fornece a moldura básica para o acesso a dados de uso geral nos sistemas operacionais Microsoft Windows.

Há três tecnologias principais no MDAC. O ActiveX Data Objects (ADO) é uma interface fácil de usar de nível alto para bancos de dados OLE. O banco de dados OLE é uma interface de nível baixo e alto desempenho para vários repositórios de dados. O ADO e o banco de dados OLE podem trabalhar com dados relacionais (tabulares) e não relacionais (hierárquicos ou de fluxo). Finalmente, o Open Database Connectivity (ODBC) é outra interface de baixo nível e alto desempenho criado especificamente para repositórios de dados relacionais.

O ADO fornece uma camada de abstração entre seu aplicativo cliente ou da camada intermediária e as interfaces de banco de dados OLE de nível baixo. O ADO usa um pequeno conjunto de objetos Automation para fornecer uma interface simples e eficiente para o banco de dados OLE. Essa interface torna o ADO a opção perfeita para desenvolvedores em linguagens de níveis mais altos, como Visual Basic e até VBScript, que desejam acessar os dados sem precisar aprender as complexidades do COM e do banco de dados OLE.

