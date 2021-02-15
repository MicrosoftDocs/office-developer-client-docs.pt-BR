---
title: Propriedade TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314284"
---
# <a name="tabledefrecordcount-property-dao"></a>Propriedade TableDef.RecordCount (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna o número total de registros de um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* .RecordCount

*expressão* Uma variável que representa um objeto **TableDef**.

## <a name="remarks"></a>Comentários

Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.

Quando você trabalhar com objetos vinculados **TableDef**, a definição da propriedade **RecordCount** será sempre –1.

