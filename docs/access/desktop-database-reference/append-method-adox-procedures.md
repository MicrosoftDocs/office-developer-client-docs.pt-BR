---
title: Método Append (Procedimentos do ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 838483d03ee57dd9a546692e130aea2360a5b83d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930613"
---
# <a name="append-method-adox-procedures"></a>Método Append (Procedimentos do ADOX)


**Aplica-se a**: Access 2013, o Office 2013


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
> Ao usar o OLE DB Provider for Microsoft Jet, o método **Append** da coleção **Procedures** permitirá que você especifique um **modo de exibição** em vez de um **procedimento** no parâmetro *comando* . O **Modo de exibição** será adicionado à fonte de dados e será adicionado à coleção **Procedures**. Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Modo de exibição** não estará mais na coleção **Procedures** e será exibido na coleção **Views**.


