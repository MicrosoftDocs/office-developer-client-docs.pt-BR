---
title: Método Append (Procedimentos do ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462319"
---
# <a name="append-method-adox-procedures"></a>Método Append (Procedimentos do ADOX)


**Aplica-se a**: Access 2013 | Office 2013


Adiciona um novo objeto [Procedure](procedure-object-adox.md) à coleção [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Procedimentos*. Acrescentar o*nome*, *comando*

## <a name="parameters"></a>Parâmetros

  - *Name*

  - Um valor **String** que especifica o nome do procedimento a ser criado e anexado.

  - *Command*

  - Um objeto [Command](command-object-ado.md) do ADO que representa o procedimento a ser criado e anexado.

## <a name="remarks"></a>Comentários

Cria um novo procedimento na fonte de dados, com o nome e os atributos especificados no objeto **Command**.

Se o texto do comando que o usuário especificar representar um modo de exibição em vez de um procedimento, o comportamento dependerá do provedor que estiver sendo usado. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.


> [!NOTE]
> <P>Ao usar o OLE DB Provider for Microsoft Jet, o método <STRONG>Append</STRONG> da coleção <STRONG>Procedures</STRONG> permitirá que você especifique um <STRONG>modo de exibição</STRONG> em vez de um <STRONG>procedimento</STRONG> no parâmetro <EM>comando</EM> . O <STRONG>Modo de exibição</STRONG> será adicionado à fonte de dados e será adicionado à coleção <STRONG>Procedures</STRONG>. Após o comando <STRONG>Append</STRONG>, se as coleções <STRONG>Procedures</STRONG> e <STRONG>Views</STRONG> forem atualizadas, o <STRONG>Modo de exibição</STRONG> não estará mais na coleção <STRONG>Procedures</STRONG> e será exibido na coleção <STRONG>Views</STRONG>.</P>


