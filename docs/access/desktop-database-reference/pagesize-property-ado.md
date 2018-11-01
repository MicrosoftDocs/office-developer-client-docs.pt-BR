---
title: Propriedade PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883271"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="a23bd-102">Propriedade PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="a23bd-102">PageSize property (ADO)</span></span>


<span data-ttu-id="a23bd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a23bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a23bd-104">Indica quantos registros formam uma página no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a23bd-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a23bd-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a23bd-105">Settings and return values</span></span>

<span data-ttu-id="a23bd-p101">Define ou retorna um valor **Long** que indica quantos registros estão presentes em uma página. O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a23bd-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="a23bd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a23bd-108">Remarks</span></span>

<span data-ttu-id="a23bd-109">Use a propriedade **PageSize** para determinar quantos registros compõem uma página lógica de dados.</span><span class="sxs-lookup"><span data-stu-id="a23bd-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="a23bd-110">Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="a23bd-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="a23bd-111">Isso é útil em cenários de servidor da web quando você deseja permitir que o usuário à página através de dados, exibindo um determinado número de registros por vez.</span><span class="sxs-lookup"><span data-stu-id="a23bd-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="a23bd-112">Essa propriedade pode ser definida a qualquer momento e seu valor será utilizado para calcular o local do primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="a23bd-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

