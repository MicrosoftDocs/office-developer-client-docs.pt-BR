---
title: Propriedade PageSize (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462362"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="5879b-102">Propriedade PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="5879b-102">PageSize Property (ADO)</span></span>


<span data-ttu-id="5879b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5879b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5879b-104">Indica quantos registros formam uma página no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5879b-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5879b-105">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5879b-105">Settings and Return Values</span></span>

<span data-ttu-id="5879b-p101">Define ou retorna um valor **Long** que indica quantos registros estão presentes em uma página. O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="5879b-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="5879b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5879b-108">Remarks</span></span>

<span data-ttu-id="5879b-p102">Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados. Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica. Isso é útil em cenários de servidores Web quando se deseja permitir que o usuário pagine os dados, exibindo um certo número de registros ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="5879b-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page. This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="5879b-112">Essa propriedade pode ser definida a qualquer momento e seu valor será utilizado para calcular o local do primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="5879b-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

