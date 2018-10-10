---
title: Propriedade TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463757"
---
# <a name="tabledefrecordcount-property-dao"></a>Propriedade TableDef.RecordCount (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna o número total de registros de um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . RecordCount

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

Em um objeto **Recordset** ou **TableDef** sem registros, a definição da propriedade **RecordCount** é 0.

Quando você trabalhar com objetos vinculados**TableDef**, a definição da propriedade **RecordCount** será sempre –1.
