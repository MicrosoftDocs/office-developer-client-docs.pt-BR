---
title: Provedores de dados (referência de banco de dados da área de trabalho do Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd2f17bcc490031625cc8f6cd0ea6d369133fa06
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462825"
---
# <a name="data-providers"></a>Provedores de dados


**Aplica-se a**: Access 2013 | Office 2013

Os provedores de dados representam diversas fontes de dados como bancos de dados SQL, arquivos sequenciais indexados, planilhas eletrônicas, repositórios de documentos e arquivos de email. Os provedores expõem os dados de maneira uniforme usando uma abstração comum chamada conjunto de linhas.

O ADO é poderoso e flexível porque consegue estabelecer conexão com qualquer um dos vários provedores de dados diferentes, e ainda expor o mesmo modelo de programação, independentemente dos recursos específicos de qualquer provedor determinado. No entanto, devido à exclusividade de cada provedor de dados, a maneira como o seu aplicativo interage com o ADO irá variar de provedor para provedor.

Por exemplo, as capacidades e os recursos do OLE DB Provider for SQL Server, que é usado para acessar os bancos de dados do Microsoft SQL Server, são consideravelmente diferentes daqueles do Microsoft OLE DB Provider for Internet Publishing, usado para acessar repositórios de arquivos em um servidor Web.

