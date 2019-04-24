---
title: Arquivos e mensagens anexados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318127"
---
# <a name="attached-files-and-messages"></a>Arquivos e mensagens anexados

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se MIME com TNEF é usado durante a codificação do conteúdo da mensagem, todas as propriedades e o conteúdo do anexo estão no fluxo TNEF. O próprio TNEF é um único arquivo binário anexado chamado winmail. dat, codificado conforme descrito para MIME sem TNEF. 
  
Se MIME for usado sem TNEF, arquivos anexados serão enviados como partes de conteúdo de mensagem MIME. O nome do arquivo é colocado no parâmetro *Name* para o cabeçalho *Content-Type* do anexo. O conjunto de caracteres para o anexo é colocado no parâmetro *charset* para o *tipo de conteúdo* ; e a codificação de transferência de conteúdo é determinada examinando todo o conteúdo do anexo. Os anexos de URL são tratados especialmente: 
  
- Se o anexo for uma URL (um arquivo anexado com extensão. URL) e o modo de acesso definido nele é FTP anônimo, ele é codificado como uma mensagem externa e o conteúdo do arquivo (a URL) é copiado para o cabeçalho da mensagem externa. *Tipo de conteúdo: mensagem/corpo externo; Access-Type = anon-FTP*  (Content-Transfer-Encoding: 7bit é assumido.) 
    
- Se apenas caracteres de 7 bits forem encontrados e nenhuma linha exceder 140 caracteres de comprimento, o anexo será texto ASCII. *Tipo de conteúdo: text/plain; charset = conteúdo US-ASCII-transferência-codificação: 7bit* 
    
- Se forem encontradas linhas longas ou até 25% de 8 bits, o conteúdo do anexo será texto e o conjunto de caracteres será determinado pela localidade. Ele deve ser escolhido dos conjuntos de caracteres definidos pelo ISO Standard 8859. *Content-Type: text/plain; charset = iso-8859-1*  (por exemplo) 
    
     *Codificação de transferência de conteúdo: quot-imprimível* 
    
- Se 25% ou mais caracteres tiverem o conjunto de bits alto, o anexo será binário. Ele é codificado usando o algoritmo base64. *Tipo de conteúdo: application/octet-stream*  (por padrão; com base na extensão de arquivo) 
    
     * Codificação de transferência de conteúdo: Base64 * 
    
Em mensagens de saída, o tipo de conteúdo deve ser derivado da extensão de três letras do nome do arquivo. Este mapeamento existe no registro do sistema; em há um valor de cadeia de caracteres chamado "tipo de conteúdo" que fornece o tipo de conteúdo MIME, se um estiver definido. Este exemplo é para um arquivo de imagem TIFF:
  
Definida
  
Software
  
O
  
Cursos
  
. tif
  
Tipo de conteúdo = "Image/TIFF"
  
Se não houver mapeamento para a extensão de arquivo, o fluxo de *aplicativo/octeto* padrão deverá ser usado. 
  
Em mensagens de entrada, o tipo de conteúdo de um anexo sempre deve ser copiado para a propriedade MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Mesmo que um FileName seja definido para um arquivo anexado, a extensão mapeada pelo tipo de conteúdo deve ser usada nas propriedades **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) e **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) .
  
O parâmetro *Name* é oficialmente preterido pela RFC 821. À medida que os padrões evoluem, a Microsoft considerará a especificação de um mapeamento alternativo para os nomes de fileanexados. 
  
As mensagens de saída anexadas são enviadas como * Content-Type: message/rfc822 * as mensagens em mensagens anexadas são codificadas recursivamente, em seu lugar adequado. Partes de conteúdo de mensagens de entrada com o *tipo de conteúdo: multipart/Digest* também são mapeadas para mensagens incorporadas. 
  
Se o uuencode com TNEF é usado durante a codificação do conteúdo da mensagem, todas as propriedades e o conteúdo do anexo estão no fluxo TNEF. O próprio TNEF é um único arquivo binário anexado chamado winmail. dat, codificado conforme descrito em Uuencode sem TNEF.
  
Se uuencode for usado sem TNEF, todos os arquivos anexados serão tratados como binários e UUencoded, seguindo o texto da mensagem. O nome do arquivo está presente no cabeçalho uuencode:
  
 iniciar o 0755 Winmail. dat 
  
 ... dados... 
  
 end 
  
As mensagens anexadas são configuradas no texto da mensagem. A hierarquia de mensagens anexadas é sempre achatada; ou seja, as mensagens em mensagens anexadas são retiradas para o nível superior.
  
Os objetos OLE incorporados são descartados.
  
As posições de renderização de anexo são transmitidas literalmente, usando a propriedade **PR_ATTACH_RENDERING** ([PIDTAGATTACHRENDERING](pidtagattachrendering-canonical-property.md)) no TNEF. Se o TNEF não for usado, eles serão perdidos. Anexos de entrada sem posição de renderização (incluindo quando não há TNEF) têm sua posição de renderização definida como 0xFFFFFFFF, ou seja, sem posição no texto da mensagem.
  
## <a name="see-also"></a>Confira também



[Mapeamento de atributos de email da Internet para propriedades MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

