---
title: Método Close (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39059a684a2a64574fc270f3fbd3797a00f66b96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465146"
---
# <a name="close-method-ado-md"></a>Método Close (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Fecha um conjunto de células aberto.

## <a name="syntax"></a>Sintaxe

*Conjunto de células*. Fechar

## <a name="remarks"></a>Comentários

O uso do método **Close** para fechar o objeto [Cellset](cellset-object-ado-md.md) liberará os dados associados, incluindo dados em objetos [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) ou [Member](member-object-ado-md.md) relacionados. O fechamento de **Cellset** não o remove da memória; você pode alterar suas configurações de propriedade e abri-lo novamente mais tarde. Para eliminar totalmente um objeto da memória, defina a variável de objeto como **Nothing**.

Posteriormente, você poderá chamar o método [Open](open-method-ado-md.md) para reabrir o **Cellset** usando a mesma cadeia de caracteres de origem ou outra. Enquanto o objeto **Cellset** estiver fechado, será gerado um erro durante a recuperação de propriedades ou a chamada de métodos que façam referência aos dados ou metadados subjacentes.

