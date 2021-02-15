---
title: Provedores de dados (referência do banco de dados da área de trabalho do Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 46d9cf80bfdd15f48d876fe63a617c9b30931fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295062"
---
# <a name="data-providers"></a>Provedores de dados


**Aplica-se ao:** Access 2013, Office 2013

Os provedores de dados representam diversas fontes de dados como bancos de dados SQL, arquivos sequenciais indexados, planilhas eletrônicas, repositórios de documentos e arquivos de email. Os provedores expõem os dados de maneira uniforme usando uma abstração comum chamada conjunto de linhas.

O ADO é poderoso e flexível porque consegue estabelecer conexão com qualquer um dos vários provedores de dados diferentes, e ainda expor o mesmo modelo de programação, independentemente dos recursos específicos de qualquer provedor determinado. No entanto, devido à exclusividade de cada provedor de dados, a maneira como o seu aplicativo interage com o ADO irá variar de provedor para provedor.

Por exemplo, os recursos do OLE DB Provider for SQL Server, que é usado para acessar bancos de dados do Microsoft SQL Server, são consideravelmente diferentes daqueles do Microsoft OLE DB Provider for Internet Publishing, que é usado para acessar os armazenamentos de arquivos em um servidor Web.

