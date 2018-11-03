---
title: Excluir método (coleções do ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a429c18890125f1c047c6356d250713ea5ea817
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944897"
---
# <a name="delete-method-adox-collections"></a>Excluir método (coleções do ADOX)


**Aplica-se a**: Access 2013, o Office 2013



Remove um objeto de uma coleção.

## <a name="syntax"></a>Sintaxe

*Coleção*. Excluir*nome*

## <a name="parameters"></a>Parâmetros

- *Name*

  - Um **Variant** que especifica o nome ou a posição ordinal (índice) do objeto a ser excluído.

## <a name="remarks"></a>Comentários

Se o *nome* não existir na coleção, ocorrerá um erro.

Para as coleções [Tables](tables-collection-adox.md) e [Users](users-collection-adox.md), ocorrerá um erro se o provedor não oferecer suporte para a exclusão de tabelas ou usuários, respectivamente. Para as coleções [Procedures](procedures-collection-adox.md) e [Views](views-collection-adox.md), o comando **Delete** falhará se o provedor não oferecer suporte para comandos persistentes.

