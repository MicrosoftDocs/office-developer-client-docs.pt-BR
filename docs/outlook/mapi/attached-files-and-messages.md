---
title: Arquivos e Mensagens Anexados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436836"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="d81ec-103">Arquivos e Mensagens Anexados</span><span class="sxs-lookup"><span data-stu-id="d81ec-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="d81ec-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d81ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d81ec-105">Se MIME com TNEF for usado durante a codificação do conteúdo da mensagem, todas as propriedades e o conteúdo do anexo estão no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="d81ec-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="d81ec-106">O próprio TNEF é um arquivo anexado binário único chamado Winmail.dat, codificado conforme descrito para MIME sem TNEF.</span><span class="sxs-lookup"><span data-stu-id="d81ec-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="d81ec-107">Se MIME for usado sem TNEF, os arquivos anexados serão enviados como partes de conteúdo de mensagem MIME.</span><span class="sxs-lookup"><span data-stu-id="d81ec-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="d81ec-108">O nome do arquivo é colocado no  *parâmetro de*  nome para o título  *do*  tipo conteúdo do anexo.</span><span class="sxs-lookup"><span data-stu-id="d81ec-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="d81ec-109">O conjunto de caracteres para o anexo é colocado no parâmetro  *charset*  para  *o tipo de conteúdo*  ; ela e a codificação de transferência de conteúdo são determinadas pela verificação de todo o conteúdo do anexo.</span><span class="sxs-lookup"><span data-stu-id="d81ec-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="d81ec-110">Os anexos de URL são tratados especialmente:</span><span class="sxs-lookup"><span data-stu-id="d81ec-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="d81ec-111">Se o anexo for uma URL (um arquivo anexado com extensão. URL), e o modo de acesso definido nele é FTP anônimo, é codificado como uma mensagem externa e o conteúdo do arquivo (a URL) é copiado para o título da mensagem externa.</span><span class="sxs-lookup"><span data-stu-id="d81ec-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="d81ec-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span><span class="sxs-lookup"><span data-stu-id="d81ec-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="d81ec-113">Se apenas caracteres de 7 bits são encontrados e nenhuma linha excede 140 caracteres de comprimento, o anexo é texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="d81ec-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="d81ec-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="d81ec-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="d81ec-115">Se linhas longas ou até 25% caracteres de 8 bits são encontrados, o conteúdo do anexo é texto e o conjunto de caracteres é determinado pela localidade.</span><span class="sxs-lookup"><span data-stu-id="d81ec-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="d81ec-116">Ele deve ser escolhido dos conjuntos de caracteres definidos pelo padrão ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="d81ec-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="d81ec-117">*Content-type: text/plain; charset=ISO-8859-1*  (por exemplo)</span><span class="sxs-lookup"><span data-stu-id="d81ec-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="d81ec-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="d81ec-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="d81ec-119">Se 25% ou mais dos caracteres têm o bit alto definido, o anexo é binário.</span><span class="sxs-lookup"><span data-stu-id="d81ec-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="d81ec-120">Ela é codificada usando o algoritmo Base64.</span><span class="sxs-lookup"><span data-stu-id="d81ec-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="d81ec-121">*Tipo de conteúdo: application/octet-stream*  (por padrão, com base na extensão de arquivo)</span><span class="sxs-lookup"><span data-stu-id="d81ec-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="d81ec-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="d81ec-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="d81ec-123">Em mensagens de saída, o tipo de conteúdo deve ser derivado da extensão de três letras do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d81ec-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="d81ec-124">Esse mapeamento existe no registro do sistema; abaixo há um valor de cadeia de caracteres chamado "Content Type" que fornece o tipo de conteúdo MIME, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="d81ec-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="d81ec-125">Este exemplo é para um arquivo de imagem TIFF:</span><span class="sxs-lookup"><span data-stu-id="d81ec-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="d81ec-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="d81ec-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="d81ec-127">Software</span><span class="sxs-lookup"><span data-stu-id="d81ec-127">Software</span></span>\
  
<span data-ttu-id="d81ec-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="d81ec-128">Microsoft</span></span>\
  
<span data-ttu-id="d81ec-129">Classes</span><span class="sxs-lookup"><span data-stu-id="d81ec-129">Classes</span></span>\
  
<span data-ttu-id="d81ec-130">.tif</span><span class="sxs-lookup"><span data-stu-id="d81ec-130">.tif</span></span>
  
<span data-ttu-id="d81ec-131">Content Type = "image/tiff"</span><span class="sxs-lookup"><span data-stu-id="d81ec-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="d81ec-132">Se não houver mapeamento para a extensão de arquivo, o fluxo  *padrão de aplicativo/octeto*  deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="d81ec-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="d81ec-133">Em mensagens de entrada, o tipo de conteúdo de um anexo sempre deve ser copiado para a propriedade MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d81ec-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="d81ec-134">Mesmo que um nome de arquivo seja definido para um arquivo anexado, a extensão mapeada pelo tipo de conteúdo deve ser usada nas propriedades **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) e **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="d81ec-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="d81ec-135">O  *parâmetro*  name foi oficialmente preterido pela RFC 821.</span><span class="sxs-lookup"><span data-stu-id="d81ec-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="d81ec-136">À medida que os padrões evoluem, a Microsoft considerará especificar um mapeamento alternativo para nomes de arquivos anexados.</span><span class="sxs-lookup"><span data-stu-id="d81ec-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="d81ec-137">As mensagens de saída anexadas são enviadas como \* Tipo de conteúdo: mensagem/rfc822 \* As mensagens dentro de mensagens anexadas são codificadas recursivamente, em seu local apropriado.</span><span class="sxs-lookup"><span data-stu-id="d81ec-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="d81ec-138">Partes de conteúdo de mensagens de entrada  *com Tipo de Conteúdo: várias partes/resumo*  também são mapeadas para mensagens incorporadas.</span><span class="sxs-lookup"><span data-stu-id="d81ec-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="d81ec-139">Se uuencode com TNEF for usado durante a codificação do conteúdo da mensagem, todas as propriedades e o conteúdo do anexo estão no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="d81ec-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="d81ec-140">O próprio TNEF é um arquivo anexado binário único chamado Winmail.dat, codificado conforme descrito para Uuencode sem TNEF.</span><span class="sxs-lookup"><span data-stu-id="d81ec-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="d81ec-141">Se uuencode for usado sem TNEF, todos os arquivos anexados serão tratados como binários e uuencoded, seguindo o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d81ec-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="d81ec-142">O nome do arquivo está presente no header uuencode:</span><span class="sxs-lookup"><span data-stu-id="d81ec-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="d81ec-143">begin 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="d81ec-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="d81ec-144">... data ...</span><span class="sxs-lookup"><span data-stu-id="d81ec-144">... data ...</span></span> 
  
 <span data-ttu-id="d81ec-145">end</span><span class="sxs-lookup"><span data-stu-id="d81ec-145">end</span></span> 
  
<span data-ttu-id="d81ec-146">As mensagens anexadas são textizadas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d81ec-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="d81ec-147">A hierarquia das mensagens anexadas é sempre nivelada; ou seja, as mensagens dentro de mensagens anexadas são retiradas para o nível superior.</span><span class="sxs-lookup"><span data-stu-id="d81ec-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="d81ec-148">Objetos OLE incorporados são descartados.</span><span class="sxs-lookup"><span data-stu-id="d81ec-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="d81ec-149">As posições de renderização de anexos são transmitidas literalmente, usando a **propriedade PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) no TNEF.</span><span class="sxs-lookup"><span data-stu-id="d81ec-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="d81ec-150">Se o TNEF não for usado, eles serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="d81ec-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="d81ec-151">Os anexos de entrada sem posição de renderização (incluindo quando não há TNEF) têm sua posição de renderização definida como 0xFFFFFFFF, ou seja, nenhuma posição no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d81ec-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d81ec-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="d81ec-152">See also</span></span>



[<span data-ttu-id="d81ec-153">Mapeamento de atributos de email da Internet para propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d81ec-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

