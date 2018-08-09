---
title: Criando um anexo de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766358"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="361a7-103">Criando um anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="361a7-103">Creating a message attachment</span></span>
  
<span data-ttu-id="361a7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="361a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="361a7-105">Um anexo da mensagem é alguns dados adicionais, como um arquivo, outra mensagem ou um objeto OLE, que você pode enviar ou salvar, juntamente com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="361a7-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="361a7-106">Cada anexo tem um conjunto de propriedades que o identifica e descreve seu tipo e como ele é processado.</span><span class="sxs-lookup"><span data-stu-id="361a7-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="361a7-107">Como destinatários, anexos de mensagens só podem ser acessados por meio da mensagem às quais eles pertencem.</span><span class="sxs-lookup"><span data-stu-id="361a7-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="361a7-108">Portanto, para um anexo ser usado, sua mensagem deve estar aberta.</span><span class="sxs-lookup"><span data-stu-id="361a7-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="361a7-109">Criar um anexo da mensagem</span><span class="sxs-lookup"><span data-stu-id="361a7-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="361a7-110">Chame o método de [IMessage::CreateAttach](imessage-createattach.md) da mensagem e passe NULL como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="361a7-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="361a7-111">**CreateAttach** retorna um número que identifica exclusivamente o novo anexo dentro da mensagem.</span><span class="sxs-lookup"><span data-stu-id="361a7-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="361a7-112">O número de anexo é armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) e é válido apenas enquanto a mensagem contendo o anexo é aberta.</span><span class="sxs-lookup"><span data-stu-id="361a7-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="361a7-113">Chame [IMAPIProp::SetProps](imapiprop-setprops.md) para definir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar como acessar o anexo.</span><span class="sxs-lookup"><span data-stu-id="361a7-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="361a7-114">**PR_ATTACH_METHOD** é necessário.</span><span class="sxs-lookup"><span data-stu-id="361a7-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="361a7-115">Defini-la como:</span><span class="sxs-lookup"><span data-stu-id="361a7-115">Set it to:</span></span> 
    
   - <span data-ttu-id="361a7-116">ATTACH_BY_VALUE se o anexo é dados binários.</span><span class="sxs-lookup"><span data-stu-id="361a7-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="361a7-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY se o anexo é um arquivo.</span><span class="sxs-lookup"><span data-stu-id="361a7-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="361a7-118">ATTACH_EMBEDDED_MSG se o anexo é uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="361a7-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="361a7-119">ATTACH_OLE se o anexo é um objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="361a7-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="361a7-120">Defina a propriedade de dados anexo apropriado:</span><span class="sxs-lookup"><span data-stu-id="361a7-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="361a7-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para dados binários e objetos OLE 1.</span><span class="sxs-lookup"><span data-stu-id="361a7-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="361a7-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para arquivos.</span><span class="sxs-lookup"><span data-stu-id="361a7-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="361a7-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensagens e objetos OLE 2.</span><span class="sxs-lookup"><span data-stu-id="361a7-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="361a7-124">Defina **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para armazenar a representação gráfica do anexo de arquivo ou anexos binários.</span><span class="sxs-lookup"><span data-stu-id="361a7-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="361a7-125">Não defini-la para os objetos OLE, qual armazenam as informações de renderização internamente, ou para mensagens anexadas.</span><span class="sxs-lookup"><span data-stu-id="361a7-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="361a7-126">Defina **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar onde o anexo deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="361a7-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="361a7-127">**PR_RENDERING_POSITION** se aplica apenas aos clientes que defina a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="361a7-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="361a7-128">Caso você ofereça suporte somente **PR_RTF_COMPRESSED**, coloque as seguintes informações de espaço reservado no stream compactado:</span><span class="sxs-lookup"><span data-stu-id="361a7-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="361a7-129">Para definir **PR_RENDERING_POSITION**, atribua um número que representa um deslocamento ordinal em caracteres, com o primeiro caractere da **PR_BODY** sendo 0, se você precisar saber onde na mensagem de que o anexo é processado ou 0xFFFFFFFF, se você não fizer isso processa anexos em **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="361a7-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="361a7-130">Definir **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar o nome curto do arquivo para um anexo de arquivo e **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar o nome do arquivo como compatíveis em uma plataforma que processa o formato de nome de arquivo longo.</span><span class="sxs-lookup"><span data-stu-id="361a7-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="361a7-131">Ambas as propriedades são opcionais.</span><span class="sxs-lookup"><span data-stu-id="361a7-131">Both properties are optional.</span></span> <span data-ttu-id="361a7-132">No entanto, se você definir **PR_ATTACH_LONG_FILENAME**, defina também **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="361a7-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="361a7-133">Defina **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar o nome do anexo que podem aparecer em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="361a7-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="361a7-134">PR_DISPLAY_NAME é opcional.</span><span class="sxs-lookup"><span data-stu-id="361a7-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="361a7-135">Definir PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="361a7-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="361a7-136">Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade com a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="361a7-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="361a7-137">Se um arquivo contém os dados e ele estiver aberto ou se você precisar controle explícito sobre o tamanho do buffer, chame **IStream::Write** em um loop para colocar os dados no stream.</span><span class="sxs-lookup"><span data-stu-id="361a7-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="361a7-138">Outra opção é chamar **OpenStreamOnFile** para criar um fluxo para acessar o arquivo de dados e, em seguida, chame o método de **IStream::CopyTo** deste fluxo para copiar os dados para o fluxo retornado por **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="361a7-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="361a7-139">Chame o método de **IStream::Commit** do novo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="361a7-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="361a7-140">Definir PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="361a7-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="361a7-141">Chame **IMAPIProp::OpenProperty** para abrir a propriedade com a interface **IStreamDocfile** para criar um fluxo que funciona com armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="361a7-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="361a7-142">**IStreamDocfile** é implementado por provedores de armazenamento de mensagem para oferecer uma maneira de alto desempenho para armazenar e recuperar o armazenamento estruturado de clientes.</span><span class="sxs-lookup"><span data-stu-id="361a7-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="361a7-143">A interface **IStreamDocfile** é igual ao **IStream**, mas o conteúdo do fluxo é garantido a ser formatado como armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="361a7-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="361a7-144">Se essa chamada tiver êxito, crie fluxo com as mesmas etapas descritas para a configuração **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="361a7-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="361a7-145">Se **OpenProperty** falhar:</span><span class="sxs-lookup"><span data-stu-id="361a7-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="361a7-146">Chame **OpenProperty** solicitando **IStorage**novamente.</span><span class="sxs-lookup"><span data-stu-id="361a7-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="361a7-147">Chame **StgOpenStorage** para abrir o objeto OLE e retornar um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="361a7-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="361a7-148">Chame o armazenamento retornado método do objeto **IStorage::CopyTo** para copiar para o objeto de armazenamento retornado da **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="361a7-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="361a7-149">Chame o método de **IStorage::Commit** do novo objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="361a7-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="361a7-150">Definir PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="361a7-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="361a7-151">Aloca uma estrutura [SPropValue](spropvalue.md) , definindo o membro **ulPropTag** como **PR_ATTACH_PATHNAME** e o membro **Value.LPSZ** à cadeia de caracteres que representa o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="361a7-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="361a7-152">Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) do anexo.</span><span class="sxs-lookup"><span data-stu-id="361a7-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="361a7-153">Se sua plataforma suporta nomes extensos de arquivos, defina **PR_ATTACH_PATHNAME** e o **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="361a7-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="361a7-154">Talvez seja necessário fazer com que um sistema operacional chamada para recuperar o nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="361a7-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="361a7-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="361a7-155">See also</span></span>

- [<span data-ttu-id="361a7-156">Anexos de MAPI</span><span class="sxs-lookup"><span data-stu-id="361a7-156">MAPI Attachments</span></span>](mapi-attachments.md)

