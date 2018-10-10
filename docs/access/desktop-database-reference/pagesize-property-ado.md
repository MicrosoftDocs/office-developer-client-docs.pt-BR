---
title: Propriedade PageSize (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462362"
---
# <a name="pagesize-property-ado"></a>Propriedade PageSize (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica quantos registros formam uma página no [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valor de retorno

Define ou retorna um valor **Long** que indica quantos registros estão presentes em uma página. O padrão é 10.

## <a name="remarks"></a>Comentários

Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidores Web quando se deseja permitir que o usuário pagine os dados, exibindo um certo número de registros ao mesmo tempo.

Essa propriedade pode ser definida a qualquer momento e seu valor será utilizado para calcular o local do primeiro registro de uma página específica.

