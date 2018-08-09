---
title: Propriedade canônica PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Modificado pela última vez: 07 de setembro de 2016'
ms.openlocfilehash: 1720e9a2eeb54daed1e559f99b0c63ce09585419
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768988"
---
# <a name="pidtagattachmethod-canonical-property"></a>Propriedade canônica PidTagAttachMethod

 
  
**Aplica-se a**: Outlook 
  
Contém uma constante definida pelo MAPI que representa a maneira como o conteúdo de um anexo pode ser acessado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_METHOD  <br/> |
|Identificador:  <br/> |0x3705  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
  
NO_ATTACHMENT 
  
> O anexo foi criado. 
    
ATTACH_BY_VALUE 
  
> A propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contém os dados do anexo. 
    
ATTACH_BY_REFERENCE 
  
> A propriedade **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) ou **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) contém um caminho totalmente qualificado que identifica o anexo a destinatários com acesso a um arquivo comuns servidor. 
    
ATTACH_BY_REF_RESOLVE 
  
> A propriedade **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo. 
    
ATTACH_BY_REF_ONLY 
  
> A propriedade **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo. 
    
ATTACH_EMBEDDED_MSG 
  
> A propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contém um objeto incorporado que dá suporte à interface **IMessage** . 
    
ATTACH_OLE 
  
> O anexo é um objeto OLE incorporado.
    
ATTACH_BY_WEBREFERENCE 
  
> O conteúdo do anexo não está na mensagem. 
    
Quando criado, todos os objetos de anexo têm um valor **PR_ATTACH_METHOD** inicial de **NO_ATTACHMENT**. 
  
Provedores de serviços e aplicativos cliente são necessárias somente para suportar o método de anexo representado pelo valor **ATTACH_BY_VALUE** . Os outros métodos de anexo são opcionais. O armazenamento de mensagens não impõe qualquer consistência entre o valor da **PR_ATTACH_METHOD** e os valores das propriedades do anexo. 
  
Nomes universais de nomenclatura (UNC) da convenção são recomendados para caminhos totalmente qualificado, que devem ser usados com **ATTACH_BY_REFERENCE** e **ATTACH_BY_REF_ONLY**. Com **ATTACH_BY_REF_RESOLVE**, um caminho absoluto é mais rápido, pois o MAPI spooler converte o anexo **ATTACH_BY_VALUE**. 
  
Se **ATTACH_BY_REFERENCE** estiver definida, **PR_ATTACH_DATA_BIN** deve estar vazio. Um gateway de saída pode ativar um anexo **ATTACH_BY_REFERENCE** em um anexo **ATTACH_BY_VALUE** , copiando os dados de anexo para a propriedade **PR_ATTACH_DATA_BIN** . 
  
Se **ATTACH_BY_REF_RESOLVE** estiver definida, **PR_ATTACH_DATA_BIN** deve estar vazio. Quando a mensagem que contém o anexo **ATTACH_BY_REF_RESOLVE** é enviada, o MAPI spooler copia os dados de anexo em um anexo **ATTACH_BY_VALUE** . Esse processo de resolução coloca os dados de anexo no **PR_ATTACH_DATA_BIN**. 
  
Se **ATTACH_BY_REF_ONLY** estiver definida, **PR_ATTACH_DATA_BIN** deve estar vazio e sistema de mensagens nunca resolve a referência de anexo. Use esse valor quando você deseja enviar o link, mas não os dados. 
  
Quando o objeto OLE está no formato OLE 2.0 **IStorage** , os dados são acessíveis através de **PR_ATTACH_DATA_OBJ**. Quando o objeto OLE está no formato 1.0 OLE **OLESTREAM** , os dados são acessíveis através de **PR_ATTACH_DATA_BIN** como um **IStream**. O tipo da codificação OLE pode ser determinado pelo valor **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para obter mais informações sobre formatos e interfaces OLE, consulte a *referência do programador do OLE* . 
  
## <a name="remarks"></a>Comentários

Quando o **PR_ATTACH_METHOD** for **ATTACH_BY_WEBREFERENCE**, o conteúdo do anexo não está na mensagem. Em vez disso, a propriedade **PR_ATTACH_LONG_FILENAME** contém uma URL absoluta para o conteúdo de anexo, que é armazenado online. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

