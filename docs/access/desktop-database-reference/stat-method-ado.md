---
title: Método STAT - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8e1193257710eb2a0a23436cfc1a36424025136
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922829"
---
# <a name="stat-method-ado"></a><span data-ttu-id="88ca5-102">Método Stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="88ca5-102">Stat method (ADO)</span></span>


<span data-ttu-id="88ca5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="88ca5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88ca5-104">Recupera informações sobre um objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="88ca5-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ca5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88ca5-105">Syntax</span></span>

<span data-ttu-id="88ca5-106">Long *stream*. Stat (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="88ca5-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="88ca5-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="88ca5-107">Return value</span></span>

<span data-ttu-id="88ca5-108">Um valor long que indica o status da operação.</span><span class="sxs-lookup"><span data-stu-id="88ca5-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="88ca5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88ca5-109">Parameters</span></span>

  - <span data-ttu-id="88ca5-110">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="88ca5-110">*StatStg*</span></span>

  - <span data-ttu-id="88ca5-p101">Uma estrutura STATSTG que será preenchida com informações sobre o fluxo. A implementação do método Stat utilizada pelo objeto Stream do ADO não preenche todos os campos da estrutura.</span><span class="sxs-lookup"><span data-stu-id="88ca5-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="88ca5-113">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="88ca5-113">*StatFlag*</span></span>

  - <span data-ttu-id="88ca5-p102">Especifica que este método não retorna alguns dos membros na estrutura STATSTG, economizando dessa forma uma operação de alocação de memória. Os valores são obtidos da enumeração STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="88ca5-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="88ca5-116">A enumeração STATFLAG tem dois valores</span><span class="sxs-lookup"><span data-stu-id="88ca5-116">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="88ca5-117">Constant</span><span class="sxs-lookup"><span data-stu-id="88ca5-117">Constant</span></span></p></th>
    <th><p><span data-ttu-id="88ca5-118">Value</span><span class="sxs-lookup"><span data-stu-id="88ca5-118">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="88ca5-119">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="88ca5-119">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="88ca5-120">0</span><span class="sxs-lookup"><span data-stu-id="88ca5-120">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="88ca5-121">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="88ca5-121">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="88ca5-122">1</span><span class="sxs-lookup"><span data-stu-id="88ca5-122">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="88ca5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="88ca5-123">Remarks</span></span>

<span data-ttu-id="88ca5-124">A versão do método Stat implementada para o objeto Stream do ADO preenche os seguintes campos da estrutura STATSTG:</span><span class="sxs-lookup"><span data-stu-id="88ca5-124">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="88ca5-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="88ca5-125">*pwcsName*</span></span>

  - <span data-ttu-id="88ca5-126">Valor de uma cadeia de caracteres contendo o nome do fluxo, caso alguma esteja disponível e o StatFlag STATFLAG\_sem nome não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="88ca5-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="88ca5-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="88ca5-127">*cbSize*</span></span>

  - <span data-ttu-id="88ca5-128">Especifica o tamanho em bytes do fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="88ca5-128">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="88ca5-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="88ca5-129">*mtime*</span></span>

  - <span data-ttu-id="88ca5-130">Indica a hora da última modificação para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="88ca5-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="88ca5-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="88ca5-131">*ctime*</span></span>

  - <span data-ttu-id="88ca5-132">Indica a hora da criação para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="88ca5-132">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="88ca5-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="88ca5-133">*atime*</span></span>

  - <span data-ttu-id="88ca5-134">Indica a hora do último acesso para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="88ca5-134">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="88ca5-135">Se STATFLAG\_sem nome for especificado no parâmetro StatFlag, o nome do fluxo não será retornado.</span><span class="sxs-lookup"><span data-stu-id="88ca5-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="88ca5-136">Se STATFLAG\_sem nome não foi especificado no parâmetro StatFlag e não há nenhum nome disponível para o fluxo atual, esse valor será f\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="88ca5-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

