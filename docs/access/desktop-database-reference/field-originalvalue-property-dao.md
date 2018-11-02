---
title: Propriedade Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d850ebcfef6ea2c08e20ed953dfcc7b5ea23cbab
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926791"
---
# <a name="fieldoriginalvalue-property-dao"></a>Propriedade Field.OriginalValue (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . OriginalValue

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Durante uma atualização em lotes otimista, pode ocorrer uma colisão quando um segundo cliente modificar o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. A propriedade **OriginalValue** contém o valor do campo na hora em que começou a última **Update** em lotes. Se esse valor não corresponder ao valor verdadeiro do banco de dados quando **Update** tentar fazer gravações no banco de dados, ocorrerá uma colisão. Quando isso acontecer, o novo valor do banco de dados será acessível por meio da propriedade **[VisibleValue](field-visiblevalue-property-dao.md)**.

