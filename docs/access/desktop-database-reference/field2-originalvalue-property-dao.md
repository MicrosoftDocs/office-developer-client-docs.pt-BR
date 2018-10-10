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
ms.openlocfilehash: a08612076ba138e5e181eec80bec2350fe27ec86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465210"
---
# <a name="field2originalvalue-property-dao"></a>Propriedade Field2.OriginalValue (DAO)


**Aplica-se a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . OriginalValue

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Durante uma atualização em lote otimista, pode ocorrer uma colisão em que um segundo cliente modifica o mesmo campo e registro enquanto o primeiro cliente recupera os dados e tenta fazer a atualização. A propriedade **OriginalValue** contém o valor do campo no momento em que o último **Update** em lote começa. Se esse valor não corresponder ao valor que está realmente no banco de dados quando o **Update** em lote tenta gravar no banco de dados, ocorrerá uma colisão. Quando isso ocorrer, o novo valor no banco de dados será acessível pela propriedade **VisibleValue**.

