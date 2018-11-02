---
title: Método SaveToFile (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 535e743a9de708b264c225f4e86390a11e1d20e5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925021"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="ab7f6-102">Método SaveToFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="ab7f6-102">SaveToFile method (ADO)</span></span>


<span data-ttu-id="ab7f6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab7f6-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ab7f6-104">Salva o conteúdo binário de um [Stream](stream-object-ado.md) para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="ab7f6-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab7f6-105">Syntax</span></span>

<span data-ttu-id="ab7f6-106">*Stream*. SaveToFile*FileName*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="ab7f6-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="ab7f6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab7f6-107">Parameters</span></span>

  - <span data-ttu-id="ab7f6-108">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ab7f6-108">*FileName*</span></span>

  - <span data-ttu-id="ab7f6-p101">Um valor **String** que contém o nome totalmente qualificado do arquivo no qual o conteúdo do **Stream** será salvo. É possível salvar em qualquer localidade local válida ou em qualquer local que você tenha acesso por um valor de UNC.</span><span class="sxs-lookup"><span data-stu-id="ab7f6-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>

  - <span data-ttu-id="ab7f6-111">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="ab7f6-111">*SaveOptions*</span></span>

  - <span data-ttu-id="ab7f6-p102">Um valor [SaveOptionsEnum](saveoptionsenum.md) que especifica se um novo arquivo deve ser criado por **SaveToFile**, se ele ainda não existir. O valor padrão é **adSaveCreateNotExists**. Com essas opções, é possível especificar que ocorre um erro se o arquivo especificado não existir. Também é possível especificar se **SaveToFile** sobrescreve o conteúdo atual de um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="ab7f6-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ab7f6-116">[!OBSERVAçãO] Se você sobrescrever um arquivo existente (quando <STRONG>adSaveCreateOverwrite</STRONG> estiver definido), <STRONG>SaveToFile</STRONG> truncará quaisquer bytes do arquivo existente original que seguem o novo <A href="eos-property-ado.md">EOS</A>.</span><span class="sxs-lookup"><span data-stu-id="ab7f6-116">If you overwrite an existing file (when <STRONG>adSaveCreateOverwrite</STRONG> is set), <STRONG>SaveToFile</STRONG> truncates any bytes from the original existing file that follow the new <A href="eos-property-ado.md">EOS</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="ab7f6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab7f6-117">Remarks</span></span>

<span data-ttu-id="ab7f6-p103">**SaveToFile** pode ser utilizado para copiar o conteúdo de um objeto **Stream** para um arquivo local. Não há alteração no conteúdo ou nas propriedades do objeto **Stream**. O objeto **Stream** deve estar aberto antes de chamar **SaveToFile**.</span><span class="sxs-lookup"><span data-stu-id="ab7f6-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="ab7f6-p104">Este método não altera a associação do objeto **Stream** com sua fonte base. O objeto **Stream** ainda estará associado à URL original ou ao **Record** que era sua fonte quando foi aberto.</span><span class="sxs-lookup"><span data-stu-id="ab7f6-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="ab7f6-123">Após uma operação **SaveToFile**, a posição atual ([Position](position-property-ado.md)) no fluxo será definida para o início do fluxo (0).</span><span class="sxs-lookup"><span data-stu-id="ab7f6-123">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

