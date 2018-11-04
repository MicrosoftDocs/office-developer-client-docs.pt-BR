---
title: Método SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba6b6ff2d373a8b05d0839d4cc113f48b47d8cad
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949583"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="18398-102">Método SubmitChanges (RDS)</span><span class="sxs-lookup"><span data-stu-id="18398-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="18398-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="18398-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18398-104">Submete as alterações pendentes do [Recordset](recordset-object-ado.md) atualizável e armazenado localmente em cache para a fonte de dados especificada na propriedade [Connect](connect-property-rds.md) ou na propriedade [URL](url-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="18398-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="18398-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18398-105">Syntax</span></span>

<span data-ttu-id="18398-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="18398-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="18398-107">*DataFactory*. SubmitChanges*Conexão*, *Recordset*</span><span class="sxs-lookup"><span data-stu-id="18398-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="18398-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18398-108">Parameters</span></span>

|<span data-ttu-id="18398-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="18398-109">Parameter</span></span>|<span data-ttu-id="18398-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="18398-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="18398-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="18398-111">*DataControl*</span></span> |<span data-ttu-id="18398-112">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="18398-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="18398-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="18398-113">*DataFactory*</span></span> |<span data-ttu-id="18398-114">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="18398-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="18398-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="18398-115">*Connection*</span></span> |<span data-ttu-id="18398-116">Um valor **String** que representa a conexão criada com a propriedade **Connect** do objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="18398-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="18398-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="18398-117">*Recordset*</span></span> |<span data-ttu-id="18398-118">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="18398-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="18398-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="18398-119">Remarks</span></span>

<span data-ttu-id="18398-120">As propriedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) e [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) devem ser definidas antes de utilizar o método **SubmitChanges** com o objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="18398-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="18398-121">Se você chamar o método [CancelUpdate](cancelupdate-method-rds.md) depois de chamar **SubmitChanges** para o mesmo objeto **Recordset**, a chamada a **CancelUpdate** falhará porque as alterações já foram confirmadas.</span><span class="sxs-lookup"><span data-stu-id="18398-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="18398-122">Apenas os registros alterados serão enviados para modificação e todas as alterações obterão êxito ou falharão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="18398-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="18398-123">Você pode usar **SubmitChanges** somente com o objeto **Rdsserver** *padrão* .</span><span class="sxs-lookup"><span data-stu-id="18398-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="18398-124">Objetos corporativos personalizados não podem utilizar esse método.</span><span class="sxs-lookup"><span data-stu-id="18398-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="18398-125">Se a propriedade **URL** foi definida, **SubmitChanges** submeterá as alterações para o local especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="18398-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

