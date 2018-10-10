---
title: Objeto Parameter (ADO)
TOCTitle: Parameter Object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7667828d2ebfdc554a7120bf495374bc50e51cfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462784"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="c0231-102">Objeto Parameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0231-102">Parameter Object (ADO)</span></span>


<span data-ttu-id="c0231-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0231-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c0231-104">Representa um parâmetro ou argumento associado ao objeto [Command](command-object-ado.md) com base em uma consulta parametrizada ou em um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="c0231-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0231-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0231-105">Remarks</span></span>

<span data-ttu-id="c0231-p101">Muitos provedores suportam comandos parametrizados. Esses são comandos no quais a ação deseja é definida uma vez, mas as variáveis (ou parâmetros) são usados para alterar alguns detalhes do comando. Por exemplo, uma instrução SQL SELECT poderia usar um parâmetro para definir os critérios de correspondência de uma cláusula WHERE e outro para definir o nome da coluna de uma cláusula SORT BY.</span><span class="sxs-lookup"><span data-stu-id="c0231-p101">Many providers support parameterized commands. These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command. For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="c0231-p102">Os objetos **Parameter** representam os parâmetros associados à consultas parametrizadas ou aos argumentos de entrada/saída e os valores de retorno de procedimentos armazenados. Dependendo da funcionalidade do provedor, alguns métodos e algumas coleções e propriedades de um objeto **Parameter** podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c0231-p102">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures. Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="c0231-111">Com as coleções, os métodos e as propriedades de um objeto **Parameter**, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c0231-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="c0231-112">Definir ou retornar o nome de um parâmetro com a propriedade [Name](name-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c0231-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="c0231-p103">Definir ou retornar o valor de um parâmetro com a propriedade [Value](value-property-ado.md). **Value** é a propriedade padrão do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="c0231-p103">Set or return the value of a parameter with the [Value](value-property-ado.md) property. **Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="c0231-115">Definir ou retornar as características do parâmetro com as propriedades [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) e [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c0231-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="c0231-116">Passar os dados binários longos ou os dados de caracteres para um parâmetro com o método [AppendChunk](appendchunk-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c0231-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="c0231-117">Acessar os atributos específicos do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c0231-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="c0231-p104">Se você souber os nomes e as propriedades dos parâmetros associados ao procedimento armazenado ou à consulta parametrizada que será chamada, use o método [CreateParameter](createparameter-method-ado.md) para criar objetos **Parameter** com as definições de propriedade adequadas e use o método [Append](append-method-ado.md) para adicioná-las à coleção [Parameters](parameters-collection-ado.md). Isso permite a definição e o retorno dos valores do parâmetro sem ter de chamar o método [Refresh](refresh-method-ado.md) na coleção **Parameters** para recuperar as informações do parâmetro a partir do provedor, uma operação de recursos potencialmente intensivos.</span><span class="sxs-lookup"><span data-stu-id="c0231-p104">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

