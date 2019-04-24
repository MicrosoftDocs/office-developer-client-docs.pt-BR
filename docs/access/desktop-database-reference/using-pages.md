---
title: Usando páginas (referência de banco de dados de área de trabalho do Access)
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
# <a name="using-pages"></a><span data-ttu-id="b301c-102">Uso de páginas</span><span class="sxs-lookup"><span data-stu-id="b301c-102">Using pages</span></span>


<span data-ttu-id="b301c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b301c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b301c-p101">Use a propriedade **PageCount** para determinar quantas páginas de dados existem no objeto **Recordset**. *Pages* são grupos de registros cujo tamanho iguala-se à configuração da propriedade **PageSize**. Mesmo que a última página esteja incompleta devido a existência de uma quantidade menor de registros do que a estabelecida pelo valor **PageSize**, ela será contada como uma página adicional no valor **PageCount**. Se o objeto **Recordset** não oferecer suporte a essa propriedade, **PageCount** será  -1 para indicar que **PageCount** é indeterminado.</span><span class="sxs-lookup"><span data-stu-id="b301c-p101">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *Pages* are groups of records whose size equals the **PageSize** property setting. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="b301c-p102">Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade **AbsolutePage** para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidores Web quando se deseja permitir que o usuário pagine os dados, exibindo um certo número de registros ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b301c-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page. This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="b301c-111">Essa propriedade pode ser definida a qualquer momento, e seu valor será usado para calcular o local do primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="b301c-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="b301c-p103">Use a propriedade **AbsolutePage** para identificar o número da página no qual o registro atual está localizado. Novamente, o provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="b301c-p103">Use the **AbsolutePage** property to identify the page number on which the current record is located. Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="b301c-p104">**AbsolutePage** é baseada em 1e igual a 1 quando o registro atual for o primeiro registro no **Recordset**. Defina-a para mover-se até o primeiro registro de uma página específica. Obtenha o número total de páginas da propriedade **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="b301c-p104">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

