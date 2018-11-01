---
title: Propriedade PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883271"
---
# <a name="pagesize-property-ado"></a>Propriedade PageSize (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica quantos registros formam uma página no [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica quantos registros estão presentes em uma página. O padrão é 10.

## <a name="remarks"></a>Comentários

Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidor da web quando você deseja permitir que o usuário à página através de dados, exibindo um determinado número de registros por vez.

Essa propriedade pode ser definida a qualquer momento e seu valor será utilizado para calcular o local do primeiro registro de uma página específica.

