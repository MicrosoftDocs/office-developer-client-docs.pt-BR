---
title: Propriedade Field2.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c88e03962789946d222acb1a6106c57d5335f3dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889781"
---
# <a name="field2originalvalue-property-dao"></a>Propriedade Field2.OriginalValue (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . OriginalValue

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Durante uma atualização em lote otimista, pode ocorrer uma colisão em que um segundo cliente modifica o mesmo campo e registro enquanto o primeiro cliente recupera os dados e tenta fazer a atualização. A propriedade **OriginalValue** contém o valor do campo no momento em que o último **Update** em lote começa. Se esse valor não corresponder ao valor que está realmente no banco de dados quando o **Update** em lote tenta gravar no banco de dados, ocorrerá uma colisão. Quando isso ocorrer, o novo valor no banco de dados será acessível pela propriedade **VisibleValue**.

