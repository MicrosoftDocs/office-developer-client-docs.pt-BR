---
title: Propriedade Source (Recordset do ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306404"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="4b597-102">Propriedade Source (Recordset do ADO)</span><span class="sxs-lookup"><span data-stu-id="4b597-102">Source property (ADO Recordset)</span></span>


<span data-ttu-id="4b597-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b597-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b597-104">Indica a fonte de dados de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4b597-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4b597-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="4b597-105">Settings and return values</span></span>

<span data-ttu-id="4b597-106">Define um valor **String** ou a referência de objeto [Command](command-object-ado.md); retorna somente um valor **String** que indica a origem do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4b597-106">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b597-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b597-107">Remarks</span></span>

<span data-ttu-id="4b597-108">Utilize a propriedade **Source** para especificar uma fonte de dados para um objeto **Recordset** utilizando uma das seguintes opções: uma variável de objeto **Command**, uma instrução SQL, um procedimento armazenado ou um nome de tabela.</span><span class="sxs-lookup"><span data-stu-id="4b597-108">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="4b597-p101">Se você definir a propriedade **Source** para um objeto **Command**, a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Recordset** herdará o valor da propriedade **ActiveConnection** para o objeto **Command** especificado. Entretanto, a leitura da propriedade **Source** não retornará o objeto **Command**; em vez disso, retornará a propriedade [CommandText](commandtext-property-ado.md) do objeto **Command** para o qual você definiu a propriedade **Source**.</span><span class="sxs-lookup"><span data-stu-id="4b597-p101">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object. However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="4b597-111">Se a propriedade **Source** for uma instrução SQL, um procedimento armazenado ou um nome de tabela, será possível otimizar o desempenho enviando o argumento adequado *Options* com a chamada do método [Open](open-method-ado-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="4b597-111">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="4b597-112">A propriedade **Source** é leitura/gravação para objetos **Recordset** fechados e somente leitura para objetos **Recordset** abertos.</span><span class="sxs-lookup"><span data-stu-id="4b597-112">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

