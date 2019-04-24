---
title: Propriedade Property. Value (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301166"
---
# <a name="propertyvalue-property-dao"></a><span data-ttu-id="ab39e-102">Propriedade Property. Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="ab39e-102">Property.Value property (DAO)</span></span>

<span data-ttu-id="ab39e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab39e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab39e-104">Define ou retorna o valor de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ab39e-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="ab39e-105">**Variant** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ab39e-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab39e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab39e-106">Syntax</span></span>

<span data-ttu-id="ab39e-107">*expressão* . Valor</span><span class="sxs-lookup"><span data-stu-id="ab39e-107">*expression* .Value</span></span>

<span data-ttu-id="ab39e-108">*expressão* Uma variável que representa um objeto **Property** .</span><span class="sxs-lookup"><span data-stu-id="ab39e-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab39e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab39e-109">Remarks</span></span>

<span data-ttu-id="ab39e-110">O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ab39e-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="ab39e-111">Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ab39e-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="ab39e-p102">A propriedade **Value** é a propriedade padrão dos objetos **Field**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="ab39e-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="ab39e-114">A tentativa de definição ou de retorno da propriedade **Value** em um contexto inadequado (por exemplo, a propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="ab39e-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="ab39e-115">Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="ab39e-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


