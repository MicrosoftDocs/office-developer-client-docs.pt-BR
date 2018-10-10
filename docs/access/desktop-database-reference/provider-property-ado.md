---
title: Propriedade Provider (ADO)
TOCTitle: Provider Property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 890f80534ff47c4dea67b34f345bce0f90328c60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461940"
---
# <a name="provider-property-ado"></a><span data-ttu-id="3fc1a-102">Propriedade Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="3fc1a-102">Provider Property (ADO)</span></span>


<span data-ttu-id="3fc1a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fc1a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3fc1a-104">Indica o nome do provedor de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3fc1a-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3fc1a-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3fc1a-105">Settings and Return Values</span></span>

<span data-ttu-id="3fc1a-106">Define ou retorna um valor **String** que indica o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="3fc1a-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc1a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fc1a-107">Remarks</span></span>

<span data-ttu-id="3fc1a-p101">Utilize a propriedade **Provider** para definir ou retornar o nome do provedor para uma conexão. Essa propriedade também pode ser definida pelo conteúdo da propriedade [ConnectionString](connectionstring-property-ado.md) ou pelo argumento \*ConnectionString \*  do método [Open](open-method-ado-connection.md); entretanto, a especificação de um provedor em mais de um local enquanto o método **Open** é chamado pode gerar resultados imprevisíveis. Se nenhum provedor for especificado, a propriedade assumirá o padrão de MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="3fc1a-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="3fc1a-p102">A propriedade **Provider** é leitura/gravação quando a conexão estiver fechada e somente leitura quando estiver aberta. A definição será efetivada somente após a abertura do objeto **Connection** ou o acesso à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. Haverá erro se a definição não for válida.</span><span class="sxs-lookup"><span data-stu-id="3fc1a-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

