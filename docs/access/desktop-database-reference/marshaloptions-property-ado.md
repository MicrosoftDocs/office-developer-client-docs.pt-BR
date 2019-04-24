---
title: Propriedade Marshaloptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289767"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="3d7d0-102">Propriedade Marshaloptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="3d7d0-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="3d7d0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d7d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d7d0-104">Indica quais registros serão empacotados de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3d7d0-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3d7d0-105">Settings And Return Values</span></span>

<span data-ttu-id="3d7d0-p101">Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d7d0-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d7d0-108">Remarks</span></span>

<span data-ttu-id="3d7d0-109">Ao usar um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados novamente na camada intermediária ou servidor Web por meio de uma técnica chamada marshaling, o processo de empacotamento e envio de parâmetros de método de interface no thread ou limites do processo.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="3d7d0-110">A definição \*\*\*\* da propriedade marshaloptions pode melhorar o desempenho quando dados remotos modificados são empacotados para atualização de volta para a camada intermediária ou servidor Web.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="3d7d0-111">**Uso do Remote Data Service** Essa propriedade é usada apenas em um **Recordset**do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

