---
title: Método SaveToFile (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706538"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="20648-102">Método SaveToFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="20648-102">SaveToFile method (ADO)</span></span>

<span data-ttu-id="20648-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="20648-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20648-104">Salva o conteúdo binário de um [Stream](stream-object-ado.md) para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="20648-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="20648-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20648-105">Syntax</span></span>

<span data-ttu-id="20648-106">*Stream*. SaveToFile*FileName*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="20648-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="20648-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20648-107">Parameters</span></span>

|<span data-ttu-id="20648-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="20648-108">Parameter</span></span>|<span data-ttu-id="20648-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="20648-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="20648-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="20648-110">*FileName*</span></span> |<span data-ttu-id="20648-p101">Um valor **String** que contém o nome totalmente qualificado do arquivo no qual o conteúdo do **Stream** será salvo. É possível salvar em qualquer localidade local válida ou em qualquer local que você tenha acesso por um valor de UNC.</span><span class="sxs-lookup"><span data-stu-id="20648-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>|
|<span data-ttu-id="20648-113">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="20648-113">*SaveOptions*</span></span> |<span data-ttu-id="20648-p102">Um valor [SaveOptionsEnum](saveoptionsenum.md) que especifica se um novo arquivo deve ser criado por **SaveToFile**, se ele ainda não existir. O valor padrão é **adSaveCreateNotExists**. Com essas opções, é possível especificar que ocorre um erro se o arquivo especificado não existir. Também é possível especificar se **SaveToFile** sobrescreve o conteúdo atual de um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="20648-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>|

> [!NOTE]
> <span data-ttu-id="20648-118">[!OBSERVAçãO] Se você sobrescrever um arquivo existente (quando **adSaveCreateOverwrite** estiver definido), **SaveToFile** truncará quaisquer bytes do arquivo existente original que seguem o novo [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="20648-118">If you overwrite an existing file (when **adSaveCreateOverwrite** is set), **SaveToFile** truncates any bytes from the original existing file that follow the new [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20648-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="20648-119">Remarks</span></span>

<span data-ttu-id="20648-p103">**SaveToFile** pode ser utilizado para copiar o conteúdo de um objeto **Stream** para um arquivo local. Não há alteração no conteúdo ou nas propriedades do objeto **Stream**. O objeto **Stream** deve estar aberto antes de chamar **SaveToFile**.</span><span class="sxs-lookup"><span data-stu-id="20648-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="20648-p104">Este método não altera a associação do objeto **Stream** com sua fonte base. O objeto **Stream** ainda estará associado à URL original ou ao **Record** que era sua fonte quando foi aberto.</span><span class="sxs-lookup"><span data-stu-id="20648-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="20648-125">Após uma operação **SaveToFile**, a posição atual ([Position](position-property-ado.md)) no fluxo será definida para o início do fluxo (0).</span><span class="sxs-lookup"><span data-stu-id="20648-125">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

