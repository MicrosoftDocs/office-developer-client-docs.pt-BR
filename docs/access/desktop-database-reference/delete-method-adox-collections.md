---
title: Método Delete (Coleções do ADOX)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea02f02270649783873f1f086bb9f39b804034a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464892"
---
# <a name="delete-method-adox-collections"></a>Método Delete (Coleções do ADOX)


**Aplica-se a**: Access 2013 | Office 2013



Remove um objeto de uma coleção.

## <a name="syntax"></a>Sintaxe

*Coleção*. Excluir*nome*

## <a name="parameters"></a>Parâmetros

  - *Name*

  - Um **Variant** que especifica o nome ou a posição ordinal (índice) do objeto a ser excluído.

## <a name="remarks"></a>Comentários

Se o *nome* não existir na coleção, ocorrerá um erro.

Para as coleções [Tables](tables-collection-adox.md) e [Users](users-collection-adox.md), ocorrerá um erro se o provedor não oferecer suporte para a exclusão de tabelas ou usuários, respectivamente. Para as coleções [Procedures](procedures-collection-adox.md) e [Views](views-collection-adox.md), o comando **Delete** falhará se o provedor não oferecer suporte para comandos persistentes.

