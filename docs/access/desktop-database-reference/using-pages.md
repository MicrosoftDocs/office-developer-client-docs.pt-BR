---
title: Usando páginas (referência do banco de dados da área de trabalho do Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305870"
---
# <a name="using-pages"></a>Uso de páginas


**Aplica-se ao:** Access 2013, Office 2013

Use a propriedade **PageCount** para determinar quantas páginas de dados existem no objeto **Recordset**. *Pages* são grupos de registros cujo tamanho iguala-se à configuração da propriedade **PageSize**. Mesmo que a última página esteja incompleta devido a existência de uma quantidade menor de registros do que a estabelecida pelo valor **PageSize**, ela será contada como uma página adicional no valor **PageCount**. Se o objeto **Recordset** não oferecer suporte a essa propriedade, **PageCount** será  -1 para indicar que **PageCount** é indeterminado.

Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade **AbsolutePage** para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidores Web quando se deseja permitir que o usuário pagine os dados, exibindo um certo número de registros ao mesmo tempo.

Essa propriedade pode ser definida a qualquer momento, e seu valor será usado para calcular o local do primeiro registro de uma página específica.

Use a propriedade **AbsolutePage** para identificar o número da página no qual o registro atual está localizado. Novamente, o provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.

**AbsolutePage** é baseada em 1e igual a 1 quando o registro atual for o primeiro registro no **Recordset**. Defina-a para mover-se até o primeiro registro de uma página específica. Obtenha o número total de páginas da propriedade **PageCount**.

