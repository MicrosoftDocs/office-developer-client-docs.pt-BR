---
title: Método Delete (Coleções do ADOX)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bfb9e12f32da56aecd9338e51d6e4656714b6c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871329"
---
# <a name="delete-method-adox-collections"></a>Método Delete (Coleções do ADOX)


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

