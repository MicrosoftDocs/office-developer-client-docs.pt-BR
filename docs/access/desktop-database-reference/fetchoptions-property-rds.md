---
title: Propriedade FetchOptions (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3e7251ba50b003b37cdeb0dd70fe4a98821d4c9
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861929"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="81db5-102">Propriedade FetchOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="81db5-102">FetchOptions Property (RDS)</span></span>


<span data-ttu-id="81db5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="81db5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="81db5-104">Indica o tipo de busca assíncrona.</span><span class="sxs-lookup"><span data-stu-id="81db5-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="81db5-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="81db5-105">Setting and Return Values</span></span>

<span data-ttu-id="81db5-106">Define ou retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="81db5-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81db5-107">Constante</span><span class="sxs-lookup"><span data-stu-id="81db5-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="81db5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="81db5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81db5-109"><strong>adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="81db5-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="81db5-p101">Todos os registros do <a href="recordset-object-ado.md">Recordset</a> são encontrados antes que o controle seja retornado ao aplicativo. O <strong>Recordset</strong> completo deve ser encontrado para que o aplicativo possa utilizá-lo de algum modo.</span><span class="sxs-lookup"><span data-stu-id="81db5-p101">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application. The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81db5-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="81db5-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="81db5-p102">O controle pode retornar ao aplicativo assim que o primeiro lote de registros for encontrado. Uma leitura subsequente do <strong>Recordset</strong> que tente acessar um registro não encontrado no primeiro lote será adiada até que o registro procurado seja realmente encontrado, quando o controle retornará ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81db5-p102">Control can return to the application as soon as the first batch of records has been fetched. A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81db5-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="81db5-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="81db5-p103">Padrão. O controle retorna imediatamente ao aplicativo enquanto os registros são encontrados em segundo plano. Se o aplicativo tentar ler um registro que ainda não foi encontrado, o registro mais próximo ao procurado será lido, e o controle retornará imediatamente, indicando que o fim atual do <strong>Recordset</strong> foi atingido. Por exemplo, uma chamada ao <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> moverá a posição atual do registro para o último registro que foi realmente encontrado, embora mais registros continuem preenchendo o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="81db5-p103">Default. Control returns immediately to the application while records are fetched in the background. If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached. For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="81db5-p104">[!OBSERVAçãO] Cada arquivo executável do lado do cliente que utilizar essas constantes deverá fornecer suas respectivas declarações. Você pode recortar e colar as declarações da constante que deseja do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="81db5-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>



## <a name="remarks"></a><span data-ttu-id="81db5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="81db5-122">Remarks</span></span>

<span data-ttu-id="81db5-123"><<<<<<< Cabeça em um aplicativo Web, você geralmente desejará usar **adcFetchAsync** (o valor padrão), porque ele fornece um melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="81db5-123"><<<<<<< HEAD In a Web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="81db5-124">Em um aplicativo cliente compilado, você geralmente usará **adcFetchBackground**.</span><span class="sxs-lookup"><span data-stu-id="81db5-124">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
<span data-ttu-id="81db5-125">=== Em um aplicativo web, você geralmente desejará usar **adcFetchAsync** (o valor padrão), porque ele fornece um melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="81db5-125">======= In a web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="81db5-126">Em um aplicativo cliente compilado, você geralmente usará **adcFetchBackground**.</span><span class="sxs-lookup"><span data-stu-id="81db5-126">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
>>>>>>> <span data-ttu-id="81db5-127">mestre</span><span class="sxs-lookup"><span data-stu-id="81db5-127">master</span></span>

