---
title: Método Refresh (ADO)
TOCTitle: Refresh Method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ea277f83c39bde4b5309a26b87961ff2325b145
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462202"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="2d3a1-102">Método Refresh (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d3a1-102">Refresh Method (ADO)</span></span>


<span data-ttu-id="2d3a1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d3a1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d3a1-104">Atualiza os objetos de uma coleção para refletir os objetos disponíveis no provedor e específicos a ele.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d3a1-105">Syntax</span></span>

<span data-ttu-id="2d3a1-106">*coleção*. Atualizar</span><span class="sxs-lookup"><span data-stu-id="2d3a1-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="2d3a1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d3a1-107">Remarks</span></span>

<span data-ttu-id="2d3a1-108">O método **Refresh** executa diferentes tarefas, dependendo da coleção a partir do qual ele for chamado.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d3a1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d3a1-109">Parameters</span></span>

<span data-ttu-id="2d3a1-p101">O uso do método **Refresh** na coleção [Parameters](command-object-ado.md) de um objeto [Command](parameters-collection-ado.md) recupera informações de parâmetro do provedor para o procedimento armazenado ou a consulta com parâmetros especificada no objeto **Command**. A coleção estará vazia para os provedores que não oferecem suporte a chamadas de procedimento armazenado ou a consultas com parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-p101">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object. The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="2d3a1-112">Defina a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Command** como um objeto [Connection](connection-object-ado.md) válido, a propriedade [CommandText](commandtext-property-ado.md) como um comando válido e a propriedade [CommandType](commandtype-property-ado.md) como **adCmdStoredProc** antes de chamar o método **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="2d3a1-113">Se você acessar a coleção **Parameters** antes de chamar o método **Refresh**, o ADO chamará o método automaticamente e preencherá a coleção para você.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2d3a1-p102">[!OBSERVAçãO] Se você usar o método <STRONG>Refresh</STRONG> para obter informações de parâmetros a partir do provedor e ele retornar um ou mais objetos <A href="parameter-object-ado.md">Parameter</A> de tipo de dados de comprimento variável, o ADO poderá alocar memória para os parâmetros com base em seu tamanho potencial máximo, causando erro durante a execução. Defina explicitamente a propriedade <A href="size-property-ado.md">Size</A> para esses parâmetros antes de chamar o método <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> a fim de evitar erros.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-p102">If you use the <STRONG>Refresh</STRONG> method to obtain parameter information from the provider and it returns one or more variable-length data type <A href="parameter-object-ado.md">Parameter</A> objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the <A href="size-property-ado.md">Size</A> property for these parameters before calling the <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> method to prevent errors.</span></span></P>



<span data-ttu-id="2d3a1-116">**Campos**</span><span class="sxs-lookup"><span data-stu-id="2d3a1-116">**Fields**</span></span>

<span data-ttu-id="2d3a1-p103">O uso do método **Refresh** na coleção **Fields** não produz nenhum efeito visível. Para recuperar as alterações da estrutura de banco de dados subjacente, use o método [Requery](requery-method-ado.md) ou, se o objeto [Recordset](recordset-object-ado.md) não oferecer suporte a indicadores, o método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2d3a1-p103">Using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="2d3a1-119">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="2d3a1-119">**Properties**</span></span>

<span data-ttu-id="2d3a1-p104">O uso do método **Refresh** em uma coleção **Properties** de alguns objetos preenche a coleção com as propriedades dinâmicas expostas pelo provedor. Essas propriedades fornecem informações sobre a a funcionalidade específica do provedor, além das propriedades internas compatíveis com o ADO.</span><span class="sxs-lookup"><span data-stu-id="2d3a1-p104">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes. These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

