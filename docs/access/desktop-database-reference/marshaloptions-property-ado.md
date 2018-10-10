---
title: Propriedade MarshalOptions (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464514"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="3b607-102">Propriedade MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b607-102">MarshalOptions Property (ADO)</span></span>


<span data-ttu-id="3b607-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b607-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3b607-104">Indica quais registros serão empacotados de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3b607-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3b607-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3b607-105">Settings And Return Values</span></span>

<span data-ttu-id="3b607-p101">Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="3b607-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b607-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b607-108">Remarks</span></span>

<span data-ttu-id="3b607-p102">Ao usar um [Recordset](recordset-object-ado.md) do lado do cliente, os registros que foram modificados no cliente são gravados de volta na camada intermediária ou no servidor Web por meio de uma técnica chamada empacotamento, o processo de empacotar e enviar parâmetros de método de interface através de limites do encadeamento ou do processo. Definir a propriedade **MarshalOptions** pode melhorar o desempenho quando dados remotos modificados são empacotados para atualização de volta à camada intermediária ou ao servidor Web.</span><span class="sxs-lookup"><span data-stu-id="3b607-p102">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries. Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>

<span data-ttu-id="3b607-111">**Uso de serviço de dados remotos** Essa propriedade é usada somente em um **Recordset**do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3b607-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

