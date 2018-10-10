---
title: Propriedade RecordCount (ADO)
TOCTitle: RecordCount Property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a619570264973fc70b7cc5bd581437a4002b00be
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464798"
---
# <a name="recordcount-property-ado"></a>Propriedade RecordCount (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o número de registros em um objeto [Recordset](recordset-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que indica o número de registros no **Recordset**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **RecordCount** para saber a quantidade de registros existentes em um objeto **Recordset**. A propriedade retorna -1 quando o ADO não puder determinar o número de registros ou se um tipo de provedor ou cursornão oferecer suporte à **RecordCount**. A leitura da propriedade **RecordCount** em um **Recordset** fechado gera um erro.

Se o objeto **Recordset** oferecer suporte a posicionamento ou indicadores aproximados  isto é, **Supports (adApproxPosition)** ou **Supports (adBookmark)**, respectivamente, ele retornará **True**  este valor será o número exato de registros do **Recordset**, independentemente de ter sido preenchido completamente. Se o objeto **Recordset** não oferecer suporte ao posicionamento aproximado, essa propriedade poderá consumir recursos de forma significativa, pois todos os registros terão que ser recuperados e contados para que um valor preciso de **RecordCount** seja retornado.

O tipo de cursor do objeto **Recordset** será afetado se o número de registros puder ser determinado. A propriedade **RecordCount** retornará -1 para um cursor somente de encaminhamento; a contagem real de um cursor estático ou de conjunto de chaves; e -1 ou a contagem real para um cursor dinâmico, dependendo da fonte de dados.

