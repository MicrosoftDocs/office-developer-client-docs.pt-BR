---
title: Método Append (Modos de exibição do ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716149"
---
# <a name="append-method-adox-views"></a>Método Append (Modos de exibição do ADOX)

**Aplica-se a**: Access 2013, o Office 2013

Cria e anexa um novo objeto [View](view-object-adox.md) à coleção [Views](views-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Modos de exibição*. Acrescentar o*nome*, *comando*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Name* |Um valor **String** que especifica o nome do modo de exibição a ser criado.|
|*Command* |Um objeto [Command](command-object-ado.md) do ADO que representa o modo de exibição a ser criado.|

## <a name="remarks"></a>Comentários

Cria um novo modo de exibição na fonte de dados, com o nome e os atributos especificados no objeto **Command**.

Se o texto do comando que o usuário especificar representar um procedimento em vez de um modo de exibição, o comportamento dependerá do provedor. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.

> [!NOTE]
> Ao usar o OLE DB Provider for Microsoft Jet, a método **Append** da coleção **Views** permitirá que você especifique um **procedimento** em vez de um **modo de exibição** no parâmetro *comando* . O **Procedimento** será adicionado à fonte de dados e será adicionado à coleção **Views**. Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Procedimento** não estará mais na coleção **Views** e será exibido na coleção **Procedures**.


