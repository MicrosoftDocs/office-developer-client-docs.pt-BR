---
title: Propriedade Source (Recordset do ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605258"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="b2e52-102">Propriedade Source (Recordset do ADO)</span><span class="sxs-lookup"><span data-stu-id="b2e52-102">Source Property (ADO Recordset)</span></span>


<span data-ttu-id="b2e52-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2e52-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b2e52-104">Indica a fonte de dados de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b2e52-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="b2e52-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="b2e52-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b2e52-106">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b2e52-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b2e52-107">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b2e52-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b2e52-108">mestre</span><span class="sxs-lookup"><span data-stu-id="b2e52-108">master</span></span>

<span data-ttu-id="b2e52-109">Define um valor **String** ou a referência de objeto [Command](command-object-ado.md); retorna somente um valor **String** que indica a origem do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b2e52-109">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e52-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e52-110">Remarks</span></span>

<span data-ttu-id="b2e52-111">Utilize a propriedade **Source** para especificar uma fonte de dados para um objeto **Recordset** utilizando uma das seguintes opções: uma variável de objeto **Command**, uma instrução SQL, um procedimento armazenado ou um nome de tabela.</span><span class="sxs-lookup"><span data-stu-id="b2e52-111">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="b2e52-p101">Se você definir a propriedade **Source** para um objeto **Command**, a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Recordset** herdará o valor da propriedade **ActiveConnection** para o objeto **Command** especificado. Entretanto, a leitura da propriedade **Source** não retornará o objeto **Command**; em vez disso, retornará a propriedade [CommandText](commandtext-property-ado.md) do objeto **Command** para o qual você definiu a propriedade **Source**.</span><span class="sxs-lookup"><span data-stu-id="b2e52-p101">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object. However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="b2e52-114">Se a propriedade **Source** é uma instrução SQL, um procedimento armazenado ou um nome de tabela, você pode otimizar o desempenho, passando o argumento adequado *Options* com a chamada do método [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="b2e52-114">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="b2e52-115">A propriedade **Source** é leitura/gravação para objetos **Recordset** fechados e somente leitura para objetos **Recordset** abertos.</span><span class="sxs-lookup"><span data-stu-id="b2e52-115">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

