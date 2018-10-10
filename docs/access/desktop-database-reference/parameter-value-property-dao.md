---
title: Propriedade Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfba253424af0ceac3ca6bf5ce244beff472702c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465287"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="be2bd-102">Propriedade Parameter.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="be2bd-102">Parameter.Value Property (DAO)</span></span>


<span data-ttu-id="be2bd-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be2bd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be2bd-p101">Define ou retorna o valor de um objeto. **Variant** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="be2bd-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="be2bd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be2bd-106">Syntax</span></span>

<span data-ttu-id="be2bd-107">*expressão* . Valor</span><span class="sxs-lookup"><span data-stu-id="be2bd-107">*expression* .Value</span></span>

<span data-ttu-id="be2bd-108">*expressão* Uma variável que representa um objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="be2bd-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be2bd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="be2bd-109">Remarks</span></span>

<span data-ttu-id="be2bd-110">O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="be2bd-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="be2bd-111">Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="be2bd-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="be2bd-p102">A propriedade **Value** é a propriedade padrão dos objetos **Field**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="be2bd-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="be2bd-114">A tentativa de definição ou de retorno da propriedade **Value** em um contexto inadequado (por exemplo, a propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="be2bd-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="be2bd-115">Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="be2bd-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>


