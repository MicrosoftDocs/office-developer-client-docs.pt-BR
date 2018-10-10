---
title: Propriedade Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 824c483f56f7b8cf4a5f09022cc3ca80101fc7f9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463347"
---
# <a name="fieldoriginalvalue-property-dao"></a>Propriedade Field.OriginalValue (DAO)


**Aplica-se a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . OriginalValue

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Durante uma atualização em lotes otimista, pode ocorrer uma colisão quando um segundo cliente modificar o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. A propriedade **OriginalValue** contém o valor do campo na hora em que começou a última **Update** em lotes. Se esse valor não corresponder ao valor verdadeiro do banco de dados quando **Update** tentar fazer gravações no banco de dados, ocorrerá uma colisão. Quando isso acontecer, o novo valor do banco de dados será acessível por meio da propriedade **[VisibleValue](field-visiblevalue-property-dao.md)**.

