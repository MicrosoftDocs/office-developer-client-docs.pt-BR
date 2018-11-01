---
title: Propriedade TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ef77f5882f4b215764a82d343d59f1f31487e58
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886113"
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

