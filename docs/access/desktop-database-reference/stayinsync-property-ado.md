---
title: Propriedade StayInSync (ADO)
TOCTitle: StayInSync Property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f492b2c3f58084be55eca4787cde486dab29ca67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463907"
---
# <a name="stayinsync-property-ado"></a>Propriedade StayInSync (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica, em um objeto [Recordset](recordset-object-ado.md) hierárquico, se a referência a registros filhos de base (ou seja, o *capítulo*) é alterada quando a posição da linha pai é alterada.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Boolean**. O valor padrão é **True**. Se for **True**, o capítulo será atualizado se o objeto pai **Recordset** alterar a posição da linha; se for **False**, o capítulo continuará a fazer referência aos dados do capítulo anterior, ainda que o objeto pai **Recordset** tenha alterado a posição da linha.

## <a name="remarks"></a>Comentários

Essa propriedade aplica-se aos Recordsets hierárquicos, como aqueles que contam com suporte do [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), e deve ser definida no **Recordset** pai antes que o **Recordset** filho seja recuperado. Essa propriedade simplifica a navegação pelos conjuntos de registros hierárquicos.

