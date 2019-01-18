---
title: Propriedade Property.Value (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e7c79fe12b3b7bfe98e0c7547f4ed2d12b148ba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713377"
---
# <a name="propertyvalue-property-dao"></a><span data-ttu-id="ec145-102">Propriedade Property.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="ec145-102">Property.Value property (DAO)</span></span>

<span data-ttu-id="ec145-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec145-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec145-p101">Define ou retorna o valor de um objeto. **Variant** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ec145-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec145-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec145-106">Syntax</span></span>

<span data-ttu-id="ec145-107">*expressão* . Valor</span><span class="sxs-lookup"><span data-stu-id="ec145-107">*expression* .Value</span></span>

<span data-ttu-id="ec145-108">*expressão* Uma variável que representa um objeto **Property** .</span><span class="sxs-lookup"><span data-stu-id="ec145-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec145-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec145-109">Remarks</span></span>

<span data-ttu-id="ec145-110">O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ec145-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="ec145-111">Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ec145-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="ec145-p102">A propriedade **Value** é a propriedade padrão dos objetos **Field**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="ec145-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="ec145-114">A tentativa de definição ou de retorno da propriedade **Value** em um contexto inadequado (por exemplo, a propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="ec145-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="ec145-115">Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="ec145-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


