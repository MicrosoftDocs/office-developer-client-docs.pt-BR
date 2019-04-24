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
description: 'Última modificação: 07 de setembro de 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327255"
---
# <a name="pidtagattachmethod-canonical-property"></a>Propriedade canônica PidTagAttachMethod

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma constante definida por MAPI que representa a maneira como o conteúdo de um anexo pode ser acessado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_METHOD  <br/> |
|Identificador:  <br/> |0x3705  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
  
NO_ATTACHMENT 
  
> O anexo acabou de ser criado. 
    
ATTACH_BY_VALUE 
  
> A propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contém os dados de anexo. 
    
ATTACH_BY_REFERENCE 
  
> A propriedade **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contém um caminho totalmente qualificado que identifica o anexo para destinatários com acesso a um arquivo comum do. 
    
ATTACH_BY_REF_RESOLVE 
  
> A propriedade **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo. 
    
ATTACH_BY_REF_ONLY 
  
> A propriedade **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo. 
    
ATTACH_EMBEDDED_MSG 
  
> A propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contém um objeto incorporado que oferece suporte à interface **IMessage** . 
    
ATTACH_OLE 
  
> O anexo é um objeto OLE incorporado.
    
ATTACH_BY_WEBREFERENCE 
  
> O conteúdo do anexo não está na mensagem. 
    
Quando criado, todos os objetos Attachment têm um valor inicial de **PR_ATTACH_METHOD** de **NO_ATTACHMENT**. 
  
Os aplicativos cliente e provedores de serviços só são necessários para dar suporte ao método Attachment representado pelo valor **ATTACH_BY_VALUE** . Os outros métodos de anexo são opcionais. O repositório de mensagens não impõe nenhuma consistência entre o valor de **PR_ATTACH_METHOD** e os valores das outras propriedades de anexo. 
  
Os nomes de convenção universal de nomenclatura (UNC) são recomendados para caminhos totalmente qualificados, que devem ser usados com o **ATTACH_BY_REFERENCE** e o **ATTACH_BY_REF_ONLY**. Com o **ATTACH_BY_REF_RESOLVE**, um caminho absoluto é mais rápido, porque o spooler MAPI converte o anexo em **ATTACH_BY_VALUE**. 
  
Se **ATTACH_BY_REFERENCE** for definido, **PR_ATTACH_DATA_BIN** deverá estar vazio. Um gateway de saída pode transformar um anexo **ATTACH_BY_REFERENCE** em um anexo **ATTACH_BY_VALUE** copiando os dados de anexo na propriedade **PR_ATTACH_DATA_BIN** . 
  
Se **ATTACH_BY_REF_RESOLVE** for definido, **PR_ATTACH_DATA_BIN** deverá estar vazio. Quando a mensagem que contém o anexo **ATTACH_BY_REF_RESOLVE** é enviada, o spooler MAPI copia os dados de anexo para um anexo **ATTACH_BY_VALUE** . Este processo de resolução coloca os dados de anexo no **PR_ATTACH_DATA_BIN**. 
  
Se **ATTACH_BY_REF_ONLY** for definido, **PR_ATTACH_DATA_BIN** deverá estar vazio, e o sistema de mensagens nunca resolverá a referência de anexo. Use este valor quando quiser enviar o link, mas não os dados. 
  
Quando o objeto OLE está no formato de **IStorage** do OLE 2,0, os dados podem ser acessados por meio do **PR_ATTACH_DATA_OBJ**. Quando o objeto OLE está no formato **OLESTREAM** OLE 1,0, os dados podem ser acessados por meio de **PR_ATTACH_DATA_BIN** como um **IStream**. O tipo de codificação OLE pode ser determinado pelo valor **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para obter mais informações sobre interfaces e formatos OLE, confira a *referência do programador de OLE* . 
  
## <a name="remarks"></a>Comentários

Quando o **PR_ATTACH_METHOD** é **ATTACH_BY_WEBREFERENCE**, o conteúdo do anexo não está na mensagem. Em vez disso, a propriedade **PR_ATTACH_LONG_FILENAME** contém uma URL absoluta para o conteúdo de anexo, que é armazenado online. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

