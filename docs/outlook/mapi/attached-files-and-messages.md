---
title: Mensagens e arquivos anexados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 489930b35d24d2691c9b9fbb59b0fa95707a0618
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766167"
---
# <a name="attached-files-and-messages"></a>Mensagens e arquivos anexados

  
  
**Aplica-se a**: Outlook 
  
Se MIME com TNEF é usado durante a codificação de conteúdo da mensagem, todas as propriedades de anexo e o conteúdo são no stream TNEF. O TNEF em si é um arquivo de anexo único, binário denominado Winmail. dat codificado conforme descrito para MIME sem TNEF. 
  
Se MIME é usado sem TNEF, arquivos anexados são enviados como partes de conteúdo de mensagem MIME. O nome de arquivo é colocado no parâmetro *name* para o cabeçalho de *tipo de conteúdo* do anexo. O conjunto de caracteres para o anexo é colocado no parâmetro *charset* para o *tipo de conteúdo* ; ele e o conteúdo de codificação de transferência são determinados pela verificação do conteúdo do anexo inteiro. Anexos de URL são tratados especialmente: 
  
- Se o anexo é uma URL (um arquivo anexado com extensão. URL) e o modo de acesso definido em que ele é FTP anônimo, ela é codificada como uma mensagem externa e o conteúdo do arquivo (a URL) é copiado para o cabeçalho da mensagem externo. *Tipo de conteúdo: mensagem/corpo externo; o tipo de acesso = anon ftp*  (Codificação de transferência de conteúdo: 7 bits é assumido.) 
    
- Se apenas caracteres de 7 bits forem encontradas e nenhuma linha excede 140 caracteres de comprimento, o anexo é de texto ASCII. *Tipo de conteúdo: texto/simples; charset = us-ascii Content-Transfer-Encoding: 7 bits* 
    
- Se as linhas de longo ou backup para 25% em caracteres de 8 bits forem encontradas, o conteúdo do anexo é texto e o conjunto de caracteres é determinado pela localidade do. Ele deve ser escolhido nos conjuntos de caracteres definidos pelo ISO 8859 standard. *Tipo de conteúdo: texto/simples; charset = ISO 8859-1*  (por exemplo) 
    
     *Conteúdo de codificação de transferência: citados-printable* 
    
- Se 25% ou mais dos caracteres tiverem definido o bit alto definido, o anexo é binário. Ela é codificada usando o algoritmo de Base64. *Tipo de conteúdo: aplicativo/octeto-fluxo*  (por padrão; com base na extensão do arquivo) 
    
     * Conteúdo de codificação de transferência: base64 * 
    
Em mensagens de saída, o tipo de conteúdo deve ser derivado de extensão de três letras do nome do arquivo. Esse mapeamento existe no registro do sistema; sob daí é um valor string, denominado "Tipo de conteúdo" que fornece o tipo de conteúdo MIME, se não houver uma definida. Este exemplo é para um arquivo de imagem TIFF:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Classes\
  
. tif
  
Tipo de conteúdo = "image tiff"
  
Se não houver nenhum mapeamento para a extensão de arquivo, o fluxo do *aplicativo/octeto* padrão deve ser usado. 
  
Em mensagens de entrada, o tipo de conteúdo para um anexo sempre deve ser copiado para a propriedade MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Mesmo se um nome de arquivo é definido para um arquivo anexado, a extensão mapeada por tipo de conteúdo deve ser usada na **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) e propriedades de **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) .
  
O parâmetro *name* oficialmente é substituído pelo RFC 821. À medida que os padrões se desenvolverem, Microsoft considerará especificando um mapeamento alternativo para nomes de arquivo anexado. 
  
Mensagens de saída de anexados são enviadas como * tipo de conteúdo: mensagem/rfc822 * mensagens em mensagens anexadas são recursivamente codificado, seus próprios lugares. Entrada de partes de conteúdo da mensagem com *tipo de conteúdo: com diversas partes/resumida* também são mapeados para mensagens inseridas. 
  
Se uuencode com TNEF é usado durante a codificação de conteúdo da mensagem, todas as propriedades de anexo e o conteúdo são no stream TNEF. O TNEF em si é um arquivo de anexo único, binário denominado Winmail. dat codificado como descrito Uuencode sem TNEF.
  
Se uuencode for usado sem TNEF, todos os arquivos anexados são tratados como binário e uuencoded, seguindo o texto da mensagem. O nome de arquivo está presente no cabeçalho uuencode:
  
 começar Winmail 0755 
  
 … dados … 
  
 end 
  
Mensagens anexadas são textized no texto da mensagem. A hierarquia das mensagens anexadas sempre é nivelada; ou seja, as mensagens em mensagens anexadas são retiradas para o nível superior.
  
Objetos OLE incorporados são descartados.
  
Posições de renderização do anexo são transmitidas literalmente, usando a propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) no TNEF. Se o TNEF não é usado, eles são perdidos. Anexos recebidos com nenhuma posição de renderização (incluindo quando não houver nenhuma TNEF) têm sua posição de renderização não definido como 0xFFFFFFFF, ou seja, nenhuma posição no texto da mensagem.
  
## <a name="see-also"></a>Confira também



[Mapeamento dos atributos de email da Internet para propriedades MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

