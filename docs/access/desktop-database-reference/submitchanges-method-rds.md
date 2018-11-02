---
title: Método SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92634f2c0d95fbe9022934d22340f768b5614a58
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923368"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="e78b8-102">Método SubmitChanges (RDS)</span><span class="sxs-lookup"><span data-stu-id="e78b8-102">SubmitChanges method (RDS)</span></span>


<span data-ttu-id="e78b8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e78b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e78b8-104">Submete as alterações pendentes do [Recordset](recordset-object-ado.md) atualizável e armazenado localmente em cache para a fonte de dados especificada na propriedade [Connect](connect-property-rds.md) ou na propriedade [URL](url-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e78b8-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e78b8-105">Syntax</span></span>

<span data-ttu-id="e78b8-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="e78b8-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="e78b8-107">*DataFactory*. SubmitChanges*Conexão*, *Recordset*</span><span class="sxs-lookup"><span data-stu-id="e78b8-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="e78b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e78b8-108">Parameters</span></span>

  - <span data-ttu-id="e78b8-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="e78b8-109">*DataControl*</span></span>

  - <span data-ttu-id="e78b8-110">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e78b8-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="e78b8-111">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="e78b8-111">*DataFactory*</span></span>

  - <span data-ttu-id="e78b8-112">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="e78b8-112">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="e78b8-113">*Connection*</span><span class="sxs-lookup"><span data-stu-id="e78b8-113">*Connection*</span></span>

  - <span data-ttu-id="e78b8-114">Um valor **String** que representa a conexão criada com a propriedade **Connect** do objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e78b8-114">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>

  - <span data-ttu-id="e78b8-115">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="e78b8-115">*Recordset*</span></span>

  - <span data-ttu-id="e78b8-116">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e78b8-116">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e78b8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e78b8-117">Remarks</span></span>

<span data-ttu-id="e78b8-118">As propriedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) e [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) devem ser definidas antes de utilizar o método **SubmitChanges** com o objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e78b8-118">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="e78b8-119">Se você chamar o método [CancelUpdate](cancelupdate-method-rds.md) depois de chamar **SubmitChanges** para o mesmo objeto **Recordset**, a chamada a **CancelUpdate** falhará porque as alterações já foram confirmadas.</span><span class="sxs-lookup"><span data-stu-id="e78b8-119">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="e78b8-120">Apenas os registros alterados serão enviados para modificação e todas as alterações obterão êxito ou falharão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e78b8-120">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="e78b8-121">Você pode usar **SubmitChanges** somente com o objeto **Rdsserver** *padrão* .</span><span class="sxs-lookup"><span data-stu-id="e78b8-121">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="e78b8-122">Objetos corporativos personalizados não podem utilizar esse método.</span><span class="sxs-lookup"><span data-stu-id="e78b8-122">Custom business objects can't use this method.</span></span>

<span data-ttu-id="e78b8-123">Se a propriedade **URL** foi definida, **SubmitChanges** submeterá as alterações para o local especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="e78b8-123">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

