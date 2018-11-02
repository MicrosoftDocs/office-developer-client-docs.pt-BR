---
title: Propriedade Recordset2.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 871d92937bb7793b09d1520d2bf3fa33b61fcaf4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919336"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="01d3b-102">Propriedade Recordset2.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="01d3b-102">Recordset2.Updatable property (DAO)</span></span>


<span data-ttu-id="01d3b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="01d3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01d3b-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01d3b-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d3b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01d3b-106">Syntax</span></span>

<span data-ttu-id="01d3b-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="01d3b-107">*expression* .Updatable</span></span>

<span data-ttu-id="01d3b-108">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="01d3b-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d3b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="01d3b-109">Remarks</span></span>

<span data-ttu-id="01d3b-110">Objetos Recordset do tipo instantâneo e somente de encaminhamento sempre retornará **False**.</span><span class="sxs-lookup"><span data-stu-id="01d3b-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="01d3b-p102">Muitos tipos de objetos podem conter campos não podem ser atualizados. Por exemplo, crie um objeto **Recordset** do tipo dynaset no qual somente alguns campos podem ser alterados. Esses campos podem ser consertados ou conter dados que são incrementados automaticamente ou o dynaset pode resultar de uma consulta que combina tabelas atualizáveis e não atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="01d3b-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="01d3b-p103">Se o objeto contém campos somente leitura, o valor da propriedade **Updatable** será **False**. Quando um ou vários campos são atualizáveis, o valor da propriedade será **True**. Você pode editar somente os campos atualizáveis. Ocorrerá um erro interceptável, se você tentar atribuir um novo valor a um campo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01d3b-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="01d3b-118">Como um objeto atualizável pode conter campos somente leitura, verifique a propriedade **DataUpdatable** de cada campo na coleção **Fields** de um objeto **Recordset** antes de editar um registro.</span><span class="sxs-lookup"><span data-stu-id="01d3b-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

