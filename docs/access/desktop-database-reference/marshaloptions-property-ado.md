---
title: Propriedade MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5983b7794677b5cc584c541289069acf282d9f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883208"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="3fb7e-102">Propriedade MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="3fb7e-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="3fb7e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fb7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fb7e-104">Indica quais registros serão empacotados de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3fb7e-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3fb7e-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3fb7e-105">Settings And Return Values</span></span>

<span data-ttu-id="3fb7e-p101">Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="3fb7e-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb7e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fb7e-108">Remarks</span></span>

<span data-ttu-id="3fb7e-109">Ao usar um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados na camada intermediária ou um servidor web por meio de uma técnica chamada marshaling, o processo de empacotamento e enviar os parâmetros de método de interface através de thread ou limites de processo.</span><span class="sxs-lookup"><span data-stu-id="3fb7e-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="3fb7e-110">A configuração da propriedade **MarshalOptions** pode melhorar o desempenho quando é empacotados de dados remotos modificados para a atualização de volta para o servidor web ou camada intermediária.</span><span class="sxs-lookup"><span data-stu-id="3fb7e-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="3fb7e-111">**Uso de serviço de dados remotos** Essa propriedade é usada somente em um **Recordset**do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3fb7e-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

