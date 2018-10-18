---
title: Método STAT - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc4ff8076ec07d065ba932ef0e0017edb97e703
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606952"
---
# <a name="stat-method-ado"></a><span data-ttu-id="86152-102">Método Stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="86152-102">Stat Method (ADO)</span></span>


<span data-ttu-id="86152-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="86152-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="86152-104">Recupera informações sobre um objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="86152-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="86152-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86152-105">Syntax</span></span>

<span data-ttu-id="86152-106">Long *stream*. Stat (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="86152-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

<span data-ttu-id="86152-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="86152-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="86152-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="86152-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="86152-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="86152-109">Return value</span></span>
>>>>>>> <span data-ttu-id="86152-110">mestre</span><span class="sxs-lookup"><span data-stu-id="86152-110">master</span></span>

<span data-ttu-id="86152-111">Um valor long que indica o status da operação.</span><span class="sxs-lookup"><span data-stu-id="86152-111">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="86152-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86152-112">Parameters</span></span>

  - <span data-ttu-id="86152-113">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="86152-113">*StatStg*</span></span>

  - <span data-ttu-id="86152-p101">Uma estrutura STATSTG que será preenchida com informações sobre o fluxo. A implementação do método Stat utilizada pelo objeto Stream do ADO não preenche todos os campos da estrutura.</span><span class="sxs-lookup"><span data-stu-id="86152-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="86152-116">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="86152-116">*StatFlag*</span></span>

  - <span data-ttu-id="86152-p102">Especifica que este método não retorna alguns dos membros na estrutura STATSTG, economizando dessa forma uma operação de alocação de memória. Os valores são obtidos da enumeração STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="86152-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="86152-119">A enumeração STATFLAG tem dois valores</span><span class="sxs-lookup"><span data-stu-id="86152-119">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="86152-120">Constant</span><span class="sxs-lookup"><span data-stu-id="86152-120">Constant</span></span></p></th>
    <th><p><span data-ttu-id="86152-121">Value</span><span class="sxs-lookup"><span data-stu-id="86152-121">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="86152-122">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="86152-122">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="86152-123">0</span><span class="sxs-lookup"><span data-stu-id="86152-123">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="86152-124">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="86152-124">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="86152-125">1</span><span class="sxs-lookup"><span data-stu-id="86152-125">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="86152-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="86152-126">Remarks</span></span>

<span data-ttu-id="86152-127">A versão do método Stat implementada para o objeto Stream do ADO preenche os seguintes campos da estrutura STATSTG:</span><span class="sxs-lookup"><span data-stu-id="86152-127">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="86152-128">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="86152-128">*pwcsName*</span></span>

  - <span data-ttu-id="86152-129">Valor de uma cadeia de caracteres contendo o nome do fluxo, caso alguma esteja disponível e o StatFlag STATFLAG\_sem nome não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="86152-129">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="86152-130">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="86152-130">*cbSize*</span></span>

  - <span data-ttu-id="86152-131">Especifica o tamanho em bytes do fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="86152-131">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="86152-132">*mtime*</span><span class="sxs-lookup"><span data-stu-id="86152-132">*mtime*</span></span>

  - <span data-ttu-id="86152-133">Indica a hora da última modificação para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="86152-133">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="86152-134">*ctime*</span><span class="sxs-lookup"><span data-stu-id="86152-134">*ctime*</span></span>

  - <span data-ttu-id="86152-135">Indica a hora da criação para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="86152-135">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="86152-136">*atime*</span><span class="sxs-lookup"><span data-stu-id="86152-136">*atime*</span></span>

  - <span data-ttu-id="86152-137">Indica a hora do último acesso para esse repositório, fluxo ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="86152-137">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="86152-138">Se STATFLAG\_sem nome for especificado no parâmetro StatFlag, o nome do fluxo não será retornado.</span><span class="sxs-lookup"><span data-stu-id="86152-138">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="86152-139">Se STATFLAG\_sem nome não foi especificado no parâmetro StatFlag e não há nenhum nome disponível para o fluxo atual, esse valor será f\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="86152-139">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

