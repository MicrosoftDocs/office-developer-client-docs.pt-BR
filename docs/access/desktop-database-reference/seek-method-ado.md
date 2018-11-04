---
title: Método - ActiveX Data Objects (ADO) Seek
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be8127ea3f298a8f137012615b1f4de656a6ea1f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949709"
---
# <a name="seek-method-ado"></a><span data-ttu-id="cc618-102">Método Seek (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc618-102">Seek method (ADO)</span></span>

<span data-ttu-id="cc618-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc618-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc618-104">Pesquisa o índice de um [Recordset](recordset-object-ado.md) para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição de linha atual para essa linha.</span><span class="sxs-lookup"><span data-stu-id="cc618-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc618-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc618-105">Syntax</span></span>

<span data-ttu-id="cc618-106">*conjunto de registros*. Seek*KeyValues*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="cc618-106">*recordset*.Seek*KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="cc618-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc618-107">Parameters</span></span>

|<span data-ttu-id="cc618-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc618-108">Parameter</span></span>|<span data-ttu-id="cc618-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc618-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cc618-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="cc618-110">*KeyValues*</span></span> |<span data-ttu-id="cc618-p101">Uma matriz de valores **Variant**. Um índice consiste em uma ou mais colunas e a matriz contém um valor a ser comparado em relação a cada coluna correspondente.</span><span class="sxs-lookup"><span data-stu-id="cc618-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="cc618-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="cc618-113">*SeekOption*</span></span> |<span data-ttu-id="cc618-114">Um valor [SeekEnum](seekenum.md) que especifica o tipo de comparação a ser feita entre as colunas do índice e os *KeyValues* correspondentes.</span><span class="sxs-lookup"><span data-stu-id="cc618-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cc618-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc618-115">Remarks</span></span>

<span data-ttu-id="cc618-116">Use o método **Seek** junto com a propriedade [Index](index-property-ado.md) se o provedor subjacente oferecer suporte aos índices no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cc618-116">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="cc618-117">Use o método **(adSeek)** [oferece suporte](supports-method-ado.md)para determinar se o provedor subjacente suporta **Seek**e o método **Supports(adIndex)** para determinar se o provedor oferece suporte a índices.</span><span class="sxs-lookup"><span data-stu-id="cc618-117">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="cc618-118">(Por exemplo, o [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) oferece suporte a **Seek** e **Index**.)</span><span class="sxs-lookup"><span data-stu-id="cc618-118">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="cc618-p103">Se **Seek** não localizar a linha desejada, nenhum erro ocorrerá e a linha será posicionada no final do **Recordset**. Defina a propriedade **Index** para o índice desejado antes de executar este método.</span><span class="sxs-lookup"><span data-stu-id="cc618-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="cc618-p104">Este método é suportado apenas com cursores do servidor. Seek não é suportado quando o valor da propriedade **CursorLocation** do objeto [Recordset](cursorlocation-property-ado.md) for **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="cc618-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="cc618-123">Este método pode ser utilizado apenas quando o objeto **Recordset** foi aberto com um [CommandTypeEnum](commandtypeenum.md) com o valor **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="cc618-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

