---
title: Método LoadFromFile (ADO)
TOCTitle: LoadFromFile Method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a2a86e739b8744f40c481eb81b86f2f1ae5fad12
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462177"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="80715-102">Método LoadFromFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="80715-102">LoadFromFile Method (ADO)</span></span>


<span data-ttu-id="80715-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="80715-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="80715-104">Carrega o conteúdo de um arquivo existente para dentro de um [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="80715-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80715-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80715-105">Syntax</span></span>

<span data-ttu-id="80715-106">*Stream*. LoadFromFile *FileName*</span><span class="sxs-lookup"><span data-stu-id="80715-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameter"></a><span data-ttu-id="80715-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80715-107">Parameter</span></span>

  - <span data-ttu-id="80715-108">*FileName*</span><span class="sxs-lookup"><span data-stu-id="80715-108">*FileName*</span></span>

  - <span data-ttu-id="80715-109">Um valor **String** que contém o nome de um arquivo a ser carregado no **Stream**.</span><span class="sxs-lookup"><span data-stu-id="80715-109">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="80715-110">*FileName* pode conter qualquer caminho e nome válidos no formato UNC.</span><span class="sxs-lookup"><span data-stu-id="80715-110">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="80715-111">Se o arquivo especificado não existir, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="80715-111">If the specified file does not exist, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="80715-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="80715-112">Remarks</span></span>

<span data-ttu-id="80715-p102">Este método pode ser utilizado para carregar o conteúdo de um arquivo local em um objeto **Stream**. Isso pode ser utilizado para fazer upload do conteúdo de um arquivo local para um servidor.</span><span class="sxs-lookup"><span data-stu-id="80715-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="80715-p103">O objeto **Stream** já deve estar aberto antes de chamar **LoadFromFile**. Este método não altera a ligação do objeto **Stream**; ele ainda estará ligado ao objeto especificado pela URL ou **Record** com o qual o **Stream** foi originalmente aberto.</span><span class="sxs-lookup"><span data-stu-id="80715-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="80715-p104">**LoadFromFile** sobrescreve o conteúdo atual do objeto **Stream** com os dados lidos do arquivo. Quaisquer bytes existentes no **Stream** serão sobrescritos pelo conteúdo do arquivo. Todos os bytes existentes anteriormente e remanescentes após o [EOS](eos-property-ado.md) criados por **LoadFromFile** são truncados.</span><span class="sxs-lookup"><span data-stu-id="80715-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="80715-120">Depois de uma chamada a **LoadFromFile**, a posição atual é definida para o início do **Stream** ([Position](position-property-ado.md) é 0).</span><span class="sxs-lookup"><span data-stu-id="80715-120">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="80715-121">Como 2 bytes podem ser adicionados no início do fluxo para codificação, o tamanho do fluxo pode não corresponder exatamente o tamanho do arquivo a partir do qual ele foi carregado.</span><span class="sxs-lookup"><span data-stu-id="80715-121">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

