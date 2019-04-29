---
title: Abrir um anexo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430620"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="62a25-103">Abrir um anexo</span><span class="sxs-lookup"><span data-stu-id="62a25-103">Opening an attachment</span></span>

<span data-ttu-id="62a25-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62a25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62a25-105">Abrir um anexo envolve a exibição dos dados.</span><span class="sxs-lookup"><span data-stu-id="62a25-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="62a25-106">Por exemplo, quando um anexo de arquivo é aberto, o conteúdo do arquivo é exibido.</span><span class="sxs-lookup"><span data-stu-id="62a25-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="62a25-107">Enquanto as mensagens e pastas são abertas usando seus identificadores de entrada, os anexos são abertos usando seus números de anexo — **PR_ATTACH_NUM** Propriedades.</span><span class="sxs-lookup"><span data-stu-id="62a25-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="62a25-108">Para obter mais informações, consulte **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62a25-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="62a25-109">Os números de anexo estão disponíveis por meio da tabela de anexos de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="62a25-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="62a25-110">Para abrir todos os anexos em uma mensagem</span><span class="sxs-lookup"><span data-stu-id="62a25-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="62a25-111">Chame o método [IMessage::](imessage-getattachmenttable.md) GetAttachmentTable da mensagem para acessar sua tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="62a25-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="62a25-112">Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="62a25-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="62a25-113">Para cada linha:</span><span class="sxs-lookup"><span data-stu-id="62a25-113">For each row:</span></span> 
    
    1. <span data-ttu-id="62a25-114">Abra o anexo passando o número de anexo representado na coluna **PR_ATTACH_NUM** em uma chamada para o método **IMessage:: OpenAttach** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="62a25-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="62a25-115">Para obter mais informações, consulte [IMessage:: OpenAttach](imessage-openattach.md).</span><span class="sxs-lookup"><span data-stu-id="62a25-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="62a25-116">**OpenAttach** retorna um ponteiro para uma implementação de **IAttach** que fornece acesso às propriedades de anexo.</span><span class="sxs-lookup"><span data-stu-id="62a25-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="62a25-117">Chame o método **IMAPIProp::** GetProps do anexo para recuperar sua propriedade **PR_ATTACH_METHOD** .</span><span class="sxs-lookup"><span data-stu-id="62a25-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="62a25-118">Para obter mais informações, consulte [IMAPIProp::](imapiprop-getprops.md) GetProps e **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62a25-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="62a25-119">Se **PR_ATTACH_METHOD** estiver definido como ATTACH_BY_REF_ONLY, chame **IMAPIProp::** GetProps para recuperar a propriedade **PR_ATTACH_PATHNAME** .</span><span class="sxs-lookup"><span data-stu-id="62a25-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="62a25-120">Para obter mais informações, consulte **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62a25-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="62a25-121">Se **PR\_ATTACH_METHOD** for definido como Attach\_BY_VALUE, chame **IMAPIProp:: OpenProperty** para abrir a **propriedade\_PR ATTACH_DATA_BIN** com a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="62a25-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="62a25-122">Consulte o exemplo de código após este procedimento.</span><span class="sxs-lookup"><span data-stu-id="62a25-122">See the sample code following this procedure.</span></span> <span data-ttu-id="62a25-123">Para obter mais informações, consulte [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) e **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62a25-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="62a25-124">Se **PR_ATTACH_METHOD** estiver definido como ATTACH_OLE e o anexo for um objeto OLE 2:</span><span class="sxs-lookup"><span data-stu-id="62a25-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="62a25-125">Chame **IMAPIProp:: OpenProperty** para abrir a **propriedade\_PR ATTACH_DATA_OBJ** com a interface **IStreamDocfile** .</span><span class="sxs-lookup"><span data-stu-id="62a25-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="62a25-126">Tente usar esta interface porque é uma implementação de **IStream** garantido para funcionar com o armazenamento estruturado com a menor quantidade de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="62a25-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="62a25-127">Para obter mais informações, consulte **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62a25-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="62a25-128">Se a \*\*\*\* chamada OpenProperty falhar, chame-a novamente para recuperar a propriedade **PR_ATTACH_DATA_BIN** com a interface **IStreamDocfile** .</span><span class="sxs-lookup"><span data-stu-id="62a25-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="62a25-129">Se essa segunda \*\*\*\* chamada OpenProperty falhar, tente novamente chamar **OpenProperty** para recuperar o **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="62a25-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="62a25-130">No enTanto, em vez de especificar **IStreamDocfile**, especifique a interface **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="62a25-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="62a25-131">Se **PR_ATTACH_METHOD** for definido como ATTACH_EMBEDDED_MSG, não é incomum que o valor de **PR_ATTACH_DATA_OBJ** contenha um erro.</span><span class="sxs-lookup"><span data-stu-id="62a25-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="62a25-132">Isso ocorre porque você e o implementador de tabelas não têm como concordar com o tipo de objeto a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="62a25-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="62a25-133">Para recuperar um ponteiro para a mensagem anexada, abra o anexo usando **IMessage:: OpenAttach**.</span><span class="sxs-lookup"><span data-stu-id="62a25-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="62a25-134">Em seguida, acesse os dados de anexo chamando o método **IMAPIProp:: OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="62a25-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="62a25-135">Para obter mais informações, consulte [IMessage:: OpenAttach](imessage-openattach.md) e [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="62a25-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="62a25-136">Você pode solicitar que um anexo seja aberto em modo de leitura/gravação ou somente leitura.</span><span class="sxs-lookup"><span data-stu-id="62a25-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="62a25-137">Somente leitura é o modo padrão, e muitos provedores de repositórios de mensagens abrem todos os anexos desse modo, independentemente do que os clientes solicitam.</span><span class="sxs-lookup"><span data-stu-id="62a25-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="62a25-138">Passe o sinalizador MAPI_BEST_ACCESS para solicitar que o provedor do repositório de mensagens conceda o nível mais alto de acesso que ele pode e, em seguida, recupere a propriedade **PR_ACCESS_LEVEL** do anexo aberto para determinar o nível de acesso que foi realmente concedido.</span><span class="sxs-lookup"><span data-stu-id="62a25-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="62a25-139">Para obter mais informações, consulte **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62a25-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="62a25-140">O exemplo a seguir mostra como abrir os dados na propriedade **PR\_ATTACH_DATA_BIN** de um anexo.</span><span class="sxs-lookup"><span data-stu-id="62a25-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="62a25-141">Ele aloca ponteiros para dois fluxos: um para o arquivo e um para o anexo.</span><span class="sxs-lookup"><span data-stu-id="62a25-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="62a25-142">A função **OpenStreamOnFile** abre o fluxo de arquivos no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="62a25-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="62a25-143">A chamada para o método **IMAPIProp:: OpenProperty** do anexo abre o fluxo de anexos no modo de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="62a25-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="62a25-144">Para obter mais informações, consulte **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)e [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="62a25-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="62a25-145">O código então copia do fluxo de arquivo para o fluxo de anexos e libera ambos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="62a25-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


