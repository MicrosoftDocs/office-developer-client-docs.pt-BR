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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722862"
---
# <a name="tabledefrecordcount-property-dao"></a>Propriedade TableDef.RecordCount (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna o número total de registros de um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . RecordCount

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

Em um objeto **Recordset** ou **TableDef** sem registros, a definição da propriedade **RecordCount** é 0.

Quando você trabalhar com objetos vinculados**TableDef**, a definição da propriedade **RecordCount** será sempre –1.

