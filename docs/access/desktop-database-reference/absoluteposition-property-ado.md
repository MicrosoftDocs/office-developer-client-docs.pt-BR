---
title: Propriedade AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281974"
---
# <a name="absoluteposition-property-ado"></a>Propriedade AbsolutePosition (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Indica a posição ordinal do registro atual de um objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** de 1 até o número de registros no objeto **Recordset**  ([RecordCount](recordcount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md).

## <a name="remarks"></a>Comentários

Para definir a propriedade **AbsolutePosition** , o ADO requer que o provedor OLE DB que você está usando implemente a interface IRowsetLocate.

O acesso à propriedade **AbsolutePosition** de um **Recordset** aberto usando um cursor somente de encaminhamento ou dinâmico provoca o erro **adErrFeatureNotAvailable**. Com outros tipos de cursor, a posição correta será retornada, desde que o provedor ofereça suporte à interface IRowsetScroll. Se o provedor não oferecer suporte a essa *interface*, a propriedade será definida como **adPosUnknown**. Consulte a documentação do seu provedor para identificar se ele oferece suporte à *IRowsetScroll*.

Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.

Assim como a propriedade [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** tem base unitária e equivale a 1 quando o registro atual é o primeiro registro no **Recordset**. É possível obter o número total de registros no objeto **Recordset** usando a propriedade [RecordCount](recordcount-property-ado.md).

Quando você define a propriedade **AbsolutePosition** , mesmo que seja um registro no cache atual, o ADO recarrega o cache com um novo grupo de registros começando com o registro que você especificou. A propriedade [CacheSize](cachesize-property-ado.md) determina o tamanho desse grupo.


> [!NOTE]
> [!OBSERVAçãO] A propriedade **AbsolutePosition** não deve ser usada como um número de registro substituto. A posição de um determinado registro é alterada quando um registro precedente é excluído. Também não há garantias de que um determinado registro terá a mesma **AbsolutePosition** se o objeto **Recordset** for consultado e aberto novamente. Os indicadores ainda são a forma recomendada de reter e retornar a uma determinada posição e são a única maneira de posicionar em todos os tipos de objetos **Recordset** .


