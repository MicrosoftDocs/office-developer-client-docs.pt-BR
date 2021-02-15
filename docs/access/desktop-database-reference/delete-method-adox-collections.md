---
title: Método Delete (Coleções do ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294075"
---
# <a name="delete-method-adox-collections"></a>Método Delete (Coleções do ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Remove um objeto de uma coleção.

## <a name="syntax"></a>Sintaxe

*Coleção*. Excluir *Nome*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Nome* |Um **Variant** que especifica o nome ou a posição ordinal (índice) do objeto a ser excluído.|

## <a name="remarks"></a>Comentários

Ocorrerá um erro se o *Nome* não existir na coleção.

Para as coleções [Tables](tables-collection-adox.md) e [Users](users-collection-adox.md), ocorrerá um erro se o provedor não oferecer suporte para a exclusão de tabelas ou usuários, respectivamente. Para as coleções [Procedures](procedures-collection-adox.md) e [Views](views-collection-adox.md), o comando **Delete** falhará se o provedor não oferecer suporte para comandos persistentes.

