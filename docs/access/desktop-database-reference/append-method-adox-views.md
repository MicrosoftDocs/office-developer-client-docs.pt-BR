---
title: Método Append (Modos de exibição do ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463700"
---
# <a name="append-method-adox-views"></a>Método Append (Modos de exibição do ADOX)


**Aplica-se a**: Access 2013 | Office 2013


Cria e anexa um novo objeto [View](view-object-adox.md) à coleção [Views](views-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Modos de exibição*. Acrescentar o*nome*, *comando*

## <a name="parameters"></a>Parâmetros

  - *Name*

  - Um valor **String** que especifica o nome do modo de exibição a ser criado.

  - *Command*

  - Um objeto [Command](command-object-ado.md) do ADO que representa o modo de exibição a ser criado.

## <a name="remarks"></a>Comentários

Cria um novo modo de exibição na fonte de dados, com o nome e os atributos especificados no objeto **Command**.

Se o texto do comando que o usuário especificar representar um procedimento em vez de um modo de exibição, o comportamento dependerá do provedor. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.


> [!NOTE]
> <P>Ao usar o OLE DB Provider for Microsoft Jet, a método <STRONG>Append</STRONG> da coleção <STRONG>Views</STRONG> permitirá que você especifique um <STRONG>procedimento</STRONG> em vez de um <STRONG>modo de exibição</STRONG> no parâmetro <EM>comando</EM> . O <STRONG>Procedimento</STRONG> será adicionado à fonte de dados e será adicionado à coleção <STRONG>Views</STRONG>. Após o comando <STRONG>Append</STRONG>, se as coleções <STRONG>Procedures</STRONG> e <STRONG>Views</STRONG> forem atualizadas, o <STRONG>Procedimento</STRONG> não estará mais na coleção <STRONG>Views</STRONG> e será exibido na coleção <STRONG>Procedures</STRONG>.</P>


