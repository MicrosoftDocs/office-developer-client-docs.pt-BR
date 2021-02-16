---
title: Criar um anexo de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405993"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="3a206-103">Criar um anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="3a206-103">Creating a message attachment</span></span>
  
<span data-ttu-id="3a206-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a206-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a206-105">Um anexo de mensagem são alguns dados adicionais, como um arquivo, outra mensagem ou um objeto OLE, que você pode enviar ou salvar junto com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3a206-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="3a206-106">Cada anexo tem uma coleção de propriedades que o identifica e descreve seu tipo e como ele é renderizado.</span><span class="sxs-lookup"><span data-stu-id="3a206-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="3a206-107">Assim como os destinatários, os anexos de mensagens só podem ser acessados por meio da mensagem à qual pertencem.</span><span class="sxs-lookup"><span data-stu-id="3a206-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="3a206-108">Portanto, para que um anexo seja usável, sua mensagem deve estar aberta.</span><span class="sxs-lookup"><span data-stu-id="3a206-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="3a206-109">Criar um anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="3a206-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="3a206-110">Chame o método [IMessage::CreateAttach](imessage-createattach.md) da mensagem e passe NULL como o identificador da interface.</span><span class="sxs-lookup"><span data-stu-id="3a206-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="3a206-111">**CreateAttach** retorna um número que identifica exclusivamente o novo anexo dentro da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3a206-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="3a206-112">O número do anexo é armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) e é válido apenas enquanto a mensagem que contém o anexo está aberta.</span><span class="sxs-lookup"><span data-stu-id="3a206-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="3a206-113">Chame [IMAPIProp::SetProps](imapiprop-setprops.md) para definir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar como acessar o anexo.</span><span class="sxs-lookup"><span data-stu-id="3a206-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="3a206-114">**PR_ATTACH_METHOD** é necessário.</span><span class="sxs-lookup"><span data-stu-id="3a206-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="3a206-115">De definida como:</span><span class="sxs-lookup"><span data-stu-id="3a206-115">Set it to:</span></span> 
    
   - <span data-ttu-id="3a206-116">ATTACH_BY_VALUE se o anexo for dados binários.</span><span class="sxs-lookup"><span data-stu-id="3a206-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="3a206-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY se o anexo for um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3a206-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="3a206-118">ATTACH_EMBEDDED_MSG se o anexo for uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3a206-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="3a206-119">ATTACH_OLE se o anexo for um objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="3a206-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="3a206-120">De definir a propriedade de dados de anexo apropriada:</span><span class="sxs-lookup"><span data-stu-id="3a206-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="3a206-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para dados binários e objetos OLE 1.</span><span class="sxs-lookup"><span data-stu-id="3a206-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="3a206-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para arquivos.</span><span class="sxs-lookup"><span data-stu-id="3a206-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="3a206-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensagens e objetos OLE 2.</span><span class="sxs-lookup"><span data-stu-id="3a206-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="3a206-124">De **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para manter a representação gráfica do anexo para anexos de arquivo ou binários.</span><span class="sxs-lookup"><span data-stu-id="3a206-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="3a206-125">Não a de definida para objetos OLE, que armazenam as informações de renderização internamente ou para mensagens anexadas.</span><span class="sxs-lookup"><span data-stu-id="3a206-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="3a206-126">De **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar onde o anexo deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="3a206-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="3a206-127">**PR_RENDERING_POSITION** aplica-se somente a clientes que definirem a **PR_BODY** propriedade.</span><span class="sxs-lookup"><span data-stu-id="3a206-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="3a206-128">Se você só tiver **suporte PR_RTF_COMPRESSED**, coloque as seguintes informações de espaço reservado no fluxo compactado:</span><span class="sxs-lookup"><span data-stu-id="3a206-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="3a206-129">Para definir **PR_RENDERING_POSITION**, atribua um número que representa um deslocamento ordinal em caracteres, com o primeiro caractere de **PR_BODY** sendo 0, se você precisar saber onde na mensagem o anexo é renderizado ou 0xFFFFFFFF, se você não renderizar anexos no **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="3a206-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="3a206-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span><span class="sxs-lookup"><span data-stu-id="3a206-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="3a206-131">Ambas as propriedades são opcionais.</span><span class="sxs-lookup"><span data-stu-id="3a206-131">Both properties are optional.</span></span> <span data-ttu-id="3a206-132">No entanto, se você definir **PR_ATTACH_LONG_FILENAME**, também definir **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="3a206-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="3a206-133">De **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar o nome do anexo que pode aparecer em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3a206-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="3a206-134">PR_DISPLAY_NAME é opcional.</span><span class="sxs-lookup"><span data-stu-id="3a206-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-pr_attach_data_bin"></a><span data-ttu-id="3a206-135">Definir PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="3a206-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="3a206-136">Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade com a interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="3a206-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="3a206-137">Se um arquivo contiver os dados e ele estiver aberto ou se você precisar de controle explícito sobre o tamanho do buffer, chame **IStream::Write** em um loop para colocar os dados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="3a206-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="3a206-138">Outra opção é chamar **OpenStreamOnFile** para criar um fluxo para acessar o arquivo de dados e, em seguida, chamar o método **IStream::CopyTo** desse fluxo para copiar os dados para o fluxo retornado por **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="3a206-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="3a206-139">Chame o método **IStream::Commit** do novo fluxo.</span><span class="sxs-lookup"><span data-stu-id="3a206-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-pr_attach_data_obj"></a><span data-ttu-id="3a206-140">Definir PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="3a206-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="3a206-141">Chame **IMAPIProp::OpenProperty** para abrir a propriedade com a interface **IStreamDocfile** para criar um fluxo que funciona com armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="3a206-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="3a206-142">**O IStreamDocfile é** implementado pelos provedores de armazenamento de mensagens para dar aos clientes uma maneira de alto desempenho de armazenar e recuperar o armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="3a206-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="3a206-143">A interface **IStreamDocfile** é igual a **IStream**, mas o conteúdo do fluxo tem garantia de ser formatado como armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="3a206-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="3a206-144">Se essa chamada for bem-sucedida, crie o fluxo com as mesmas etapas descritas para definir **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="3a206-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="3a206-145">Se **OpenProperty** falhar:</span><span class="sxs-lookup"><span data-stu-id="3a206-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="3a206-146">Chame **OpenProperty** novamente solicitando **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="3a206-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="3a206-147">Chame **StgOpenStorage** para abrir o objeto OLE e retornar um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a206-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="3a206-148">Chame o método **IStorage::CopyTo** do objeto de armazenamento retornado para copiar para o objeto de armazenamento retornado de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="3a206-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="3a206-149">Chame o método **IStorage::Commit do** novo objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a206-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-pr_attach_pathname"></a><span data-ttu-id="3a206-150">Definir PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="3a206-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="3a206-151">Aloce uma [estrutura SPropValue,](spropvalue.md) definindo o **membro ulPropTag** como **PR_ATTACH_PATHNAME** e o membro **Value.LPSZ** para a cadeia de caracteres que representa o nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3a206-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="3a206-152">Chame o método [IMAPIProp::SetProps do](imapiprop-setprops.md) anexo.</span><span class="sxs-lookup"><span data-stu-id="3a206-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3a206-153">Se sua plataforma oferece suporte a nomes de arquivo longos, **de** definida PR_ATTACH_PATHNAME e **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="3a206-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="3a206-154">Pode ser necessário fazer uma chamada do sistema operacional para recuperar o nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="3a206-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a206-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a206-155">See also</span></span>

- [<span data-ttu-id="3a206-156">Anexos MAPI</span><span class="sxs-lookup"><span data-stu-id="3a206-156">MAPI Attachments</span></span>](mapi-attachments.md)

