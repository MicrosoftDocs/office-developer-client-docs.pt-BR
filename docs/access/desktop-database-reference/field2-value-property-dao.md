---
title: Propriedade Field2.Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6646a961950249c4f06d8cd91b57cbce4746fb1f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874290"
---
# <a name="field2value-property-dao"></a><span data-ttu-id="2ce9b-102">Propriedade Field2.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ce9b-102">Field2.Value Property (DAO)</span></span>


<span data-ttu-id="2ce9b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ce9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ce9b-p101">Define ou retorna o valor de um objeto. **Variant** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2ce9b-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce9b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ce9b-106">Syntax</span></span>

<span data-ttu-id="2ce9b-107">*expressão* . Valor</span><span class="sxs-lookup"><span data-stu-id="2ce9b-107">*expression* .Value</span></span>

<span data-ttu-id="2ce9b-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="2ce9b-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce9b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ce9b-109">Remarks</span></span>

<span data-ttu-id="2ce9b-110">O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2ce9b-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="2ce9b-111">Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2ce9b-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="2ce9b-p102">A propriedade **Value** é a propriedade padrão dos objetos **Field2**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="2ce9b-p102">The **Value** property is the default property of the **Field2**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="2ce9b-114">A tentativa de definição ou de retorno da propriedade **Value** em um contexto inapropriado (por exemplo, a propriedade **Value** de um objeto **Field2** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="2ce9b-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field2** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2ce9b-115">Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="2ce9b-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>


