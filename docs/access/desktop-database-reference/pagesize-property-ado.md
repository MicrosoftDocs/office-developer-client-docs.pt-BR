---
title: Propriedade PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288130"
---
# <a name="pagesize-property-ado"></a>Propriedade PageSize (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica quantos registros formam uma página no [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica quantos registros estão presentes em uma página. O padrão é 10.

## <a name="remarks"></a>Comentários

Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidor Web quando você deseja permitir que o usuário acesse os dados, exibindo um certo número de registros por vez.

Essa propriedade pode ser definida a qualquer momento, e seu valor será usado para calcular o local do primeiro registro de uma página específica.

