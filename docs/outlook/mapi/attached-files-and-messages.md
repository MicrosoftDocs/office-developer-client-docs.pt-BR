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
# <a name="attached-files-and-messages"></a>Arquivos e Mensagens Anexados

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se MIME com TNEF for usado durante a codificação do conteúdo da mensagem, todas as propriedades e o conteúdo do anexo estão no fluxo TNEF. O próprio TNEF é um arquivo anexado binário único chamado Winmail.dat, codificado conforme descrito para MIME sem TNEF. 
  
Se MIME for usado sem TNEF, os arquivos anexados serão enviados como partes de conteúdo de mensagem MIME. O nome do arquivo é colocado no  *parâmetro de*  nome para o título  *do*  tipo conteúdo do anexo. O conjunto de caracteres para o anexo é colocado no parâmetro  *charset*  para  *o tipo de conteúdo*  ; ela e a codificação de transferência de conteúdo são determinadas pela verificação de todo o conteúdo do anexo. Os anexos de URL são tratados especialmente: 
  
- Se o anexo for uma URL (um arquivo anexado com extensão. URL), e o modo de acesso definido nele é FTP anônimo, é codificado como uma mensagem externa e o conteúdo do arquivo (a URL) é copiado para o título da mensagem externa. *Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.) 
    
- Se apenas caracteres de 7 bits são encontrados e nenhuma linha excede 140 caracteres de comprimento, o anexo é texto ASCII. *Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit* 
    
- Se linhas longas ou até 25% caracteres de 8 bits são encontrados, o conteúdo do anexo é texto e o conjunto de caracteres é determinado pela localidade. Ele deve ser escolhido dos conjuntos de caracteres definidos pelo padrão ISO 8859. *Content-type: text/plain; charset=ISO-8859-1*  (por exemplo) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Se 25% ou mais dos caracteres têm o bit alto definido, o anexo é binário. Ela é codificada usando o algoritmo Base64. *Tipo de conteúdo: application/octet-stream*  (por padrão, com base na extensão de arquivo) 
    
     * Content-Transfer-Encoding: base64 * 
    
Em mensagens de saída, o tipo de conteúdo deve ser derivado da extensão de três letras do nome do arquivo. Esse mapeamento existe no registro do sistema; abaixo há um valor de cadeia de caracteres chamado "Content Type" que fornece o tipo de conteúdo MIME, se um estiver definido. Este exemplo é para um arquivo de imagem TIFF:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Classes\
  
.tif
  
Content Type = "image/tiff"
  
Se não houver mapeamento para a extensão de arquivo, o fluxo  *padrão de aplicativo/octeto*  deverá ser usado. 
  
Em mensagens de entrada, o tipo de conteúdo de um anexo sempre deve ser copiado para a propriedade MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Mesmo que um nome de arquivo seja definido para um arquivo anexado, a extensão mapeada pelo tipo de conteúdo deve ser usada nas propriedades **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) e **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) .
  
O  *parâmetro*  name foi oficialmente preterido pela RFC 821. À medida que os padrões evoluem, a Microsoft considerará especificar um mapeamento alternativo para nomes de arquivos anexados. 
  
As mensagens de saída anexadas são enviadas como * Tipo de conteúdo: mensagem/rfc822 * As mensagens dentro de mensagens anexadas são codificadas recursivamente, em seu local apropriado. Partes de conteúdo de mensagens de entrada  *com Tipo de Conteúdo: várias partes/resumo*  também são mapeadas para mensagens incorporadas. 
  
Se uuencode com TNEF for usado durante a codificação do conteúdo da mensagem, todas as propriedades e o conteúdo do anexo estão no fluxo TNEF. O próprio TNEF é um arquivo anexado binário único chamado Winmail.dat, codificado conforme descrito para Uuencode sem TNEF.
  
Se uuencode for usado sem TNEF, todos os arquivos anexados serão tratados como binários e uuencoded, seguindo o texto da mensagem. O nome do arquivo está presente no header uuencode:
  
 begin 0755 Winmail.dat 
  
 ... data ... 
  
 end 
  
As mensagens anexadas são textizadas no texto da mensagem. A hierarquia das mensagens anexadas é sempre nivelada; ou seja, as mensagens dentro de mensagens anexadas são retiradas para o nível superior.
  
Objetos OLE incorporados são descartados.
  
As posições de renderização de anexos são transmitidas literalmente, usando a **propriedade PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) no TNEF. Se o TNEF não for usado, eles serão perdidos. Os anexos de entrada sem posição de renderização (incluindo quando não há TNEF) têm sua posição de renderização definida como 0xFFFFFFFF, ou seja, nenhuma posição no texto da mensagem.
  
## <a name="see-also"></a>Confira também



[Mapeamento de atributos de email da Internet para propriedades MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

