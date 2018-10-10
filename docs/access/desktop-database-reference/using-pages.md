---
title: Usando páginas (referência de banco de dados da área de trabalho do Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b25123698f39e602b59a2f5cd6bd9a2f0595addb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465170"
---
# <a name="using-pages"></a>Usando páginas


**Aplica-se a**: Access 2013 | Office 2013

Utilize a propriedade **PageCount** para determinar a quantidade de páginas de dados contida no objeto **Recordset**. *Páginas* são grupos de registros cujo tamanho é igual a configuração da propriedade **PageSize** . Mesmo que a última página esteja incompleta devido a existência de uma quantidade menor de registros do que a estabelecida pelo valor **PageSize**, ela será contada como uma página adicional no valor **PageCount**. Se o objeto **Recordset** não oferecer suporte a essa propriedade, **PageCount** será -1 para indicar que **PageCount** é indeterminado.

Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade **AbsolutePage** para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidores Web quando se deseja permitir que o usuário pagine os dados, exibindo um certo número de registros ao mesmo tempo.

Essa propriedade pode ser definida a qualquer momento, e seu valor será usado para calcular o local do primeiro registro de uma página específica.

Use a propriedade **AbsolutePage** para identificar o número da página no qual o registro atual está localizado. Novamente, o provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.

**AbsolutePage** é baseada em 1e igual a 1 quando o registro atual for o primeiro registro no **Recordset**. Defina-a para mover-se até o primeiro registro de uma página específica. Obtenha o número total de páginas da propriedade **PageCount**.

