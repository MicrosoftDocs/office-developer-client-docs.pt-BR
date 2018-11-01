---
title: Propriedade Count (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c710b02678940d898f910ef5215d879cd6ded163
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880856"
---
# <a name="count-property-ado"></a>Propriedade Count (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica a quantidade de objetos em uma coleção.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long**.

## <a name="remarks"></a>Comentários

Use a propriedade **Count** para determinar quantos objetos existem em uma determinada coleção.

Como a numeração dos membros de uma coleção começa com zero, você deve sempre codificar loops que comecem no membro zero e terminem com o valor da propriedade **Count** menos 1. Se estiver usando o Microsoft Visual Basic e quiser executar um loop utilizando os membros da coleção sem verificar a propriedade **Count**, use o comando **For** **Each...Next**.

Se a propriedade **Count** for zero, não haverá objetos na coleção.

