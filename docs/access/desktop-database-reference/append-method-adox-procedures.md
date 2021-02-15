---
title: Método Append (Procedimentos do ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297078"
---
# <a name="append-method-adox-procedures"></a>Método Append (Procedimentos do ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um novo objeto [Procedure](procedure-object-adox.md) à coleção [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Procedimentos*. Append *Name*, *Command*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Nome* |Um valor **String** que especifica o nome do procedimento a ser criado e anexado.|
|*Command* |Um objeto [Command](command-object-ado.md) do ADO que representa o procedimento a ser criado e anexado.|

## <a name="remarks"></a>Comentários

Cria um novo procedimento na fonte de dados, com o nome e os atributos especificados no objeto **Command**.

Se o texto do comando que o usuário especificar representar um modo de exibição em vez de um procedimento, o comportamento dependerá do provedor que estiver sendo usado. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.

> [!NOTE]
> Quando for usado o OLE DB Provider for Microsoft Jet, o método **Append** da coleção **Procedures** permitirá que você especifique um **Modo de exibição** em vez de um **Procedimento** no parâmetro *Command*. O **Modo de exibição** será adicionado à fonte de dados e será adicionado à coleção **Procedures**. Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Modo de exibição** não estará mais na coleção **Procedures** e será exibido na coleção **Views**.


