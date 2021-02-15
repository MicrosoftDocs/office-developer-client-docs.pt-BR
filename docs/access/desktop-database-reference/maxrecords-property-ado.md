---
title: Propriedade MaxRecords (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289718"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="8617d-102">Propriedade MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="8617d-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="8617d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8617d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8617d-104">Indica o número máximo de registros a serem retornados a um [Recordset](recordset-object-ado.md) a partir de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="8617d-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8617d-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8617d-105">Settings and return values</span></span>

<span data-ttu-id="8617d-106">Define ou retorna um valor **Long** que indica o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="8617d-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="8617d-107">O padrão é zero (sem limite).</span><span class="sxs-lookup"><span data-stu-id="8617d-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="8617d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8617d-108">Remarks</span></span>

<span data-ttu-id="8617d-p102">Use a propriedade **MaxRecords** para limitar o número de registros que o provedor retorna da fonte de dados. A definição padrão dessa propriedade é zero, o que significa que o provedor retorna todos os registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="8617d-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="8617d-111">A propriedade **MaxRecords** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="8617d-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

