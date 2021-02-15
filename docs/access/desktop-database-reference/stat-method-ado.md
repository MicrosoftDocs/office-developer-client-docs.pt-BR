---
title: Método Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308544"
---
# <a name="stat-method-ado"></a><span data-ttu-id="8723f-102">Método Stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="8723f-102">Stat method (ADO)</span></span>

<span data-ttu-id="8723f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8723f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8723f-104">Recupera informações sobre um objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="8723f-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8723f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8723f-105">Syntax</span></span>

<span data-ttu-id="8723f-106">Fluxo *longo.* Stat(*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="8723f-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="8723f-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8723f-107">Return value</span></span>

<span data-ttu-id="8723f-108">Um valor long que indica o status da operação.</span><span class="sxs-lookup"><span data-stu-id="8723f-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="8723f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8723f-109">Parameters</span></span>

|<span data-ttu-id="8723f-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="8723f-110">Parameter</span></span>|<span data-ttu-id="8723f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8723f-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8723f-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="8723f-112">*StatStg*</span></span> |<span data-ttu-id="8723f-p101">Uma estrutura STATSTG que será preenchida com informações sobre o fluxo. A implementação do método Stat utilizada pelo objeto Stream do ADO não preenche todos os campos da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8723f-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="8723f-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="8723f-115">*StatFlag*</span></span> |<span data-ttu-id="8723f-p102">Especifica que este método não retorna alguns dos membros na estrutura STATSTG, economizando dessa forma uma operação de alocação de memória. Os valores são obtidos da enumeração STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="8723f-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="8723f-118">A enumeração STATFLAG tem dois valores:</span><span class="sxs-lookup"><span data-stu-id="8723f-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="8723f-119">- STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="8723f-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="8723f-120">- STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="8723f-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="8723f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8723f-121">Remarks</span></span>

<span data-ttu-id="8723f-122">A versão do método Stat implementada para o objeto Stream do ADO preenche os seguintes campos da estrutura STATSTG:</span><span class="sxs-lookup"><span data-stu-id="8723f-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="8723f-123">Campo</span><span class="sxs-lookup"><span data-stu-id="8723f-123">Field</span></span>|<span data-ttu-id="8723f-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="8723f-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8723f-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="8723f-125">*pwcsName*</span></span> |<span data-ttu-id="8723f-126">Uma cadeia de caracteres que contém o nome do fluxo, se um estiver disponível e o valor StatFlag NONAME não \_ foi especificado.</span><span class="sxs-lookup"><span data-stu-id="8723f-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="8723f-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="8723f-127">*cbSize*</span></span> |<span data-ttu-id="8723f-128">Especifica o tamanho em bytes do fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="8723f-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="8723f-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="8723f-129">*mtime*</span></span> |<span data-ttu-id="8723f-130">Indica a hora da última modificação para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="8723f-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="8723f-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="8723f-131">*ctime*</span></span> |<span data-ttu-id="8723f-132">Indica a hora da criação para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="8723f-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="8723f-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="8723f-133">*atime*</span></span> |<span data-ttu-id="8723f-134">Indica a hora do último acesso para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="8723f-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="8723f-135">Se STATFLAG NONAME for especificado no parâmetro \_ StatFlag, o nome do fluxo não será retornado.</span><span class="sxs-lookup"><span data-stu-id="8723f-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="8723f-136">Se STATFLAG NONAME não foi especificado no parâmetro StatFlag e não há nenhum nome disponível para o fluxo atual, esse valor será \_ E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="8723f-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

