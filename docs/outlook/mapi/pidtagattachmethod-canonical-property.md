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
  
> A **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contém os dados do anexo. 
    
ATTACH_BY_REFERENCE 
  
> A **propriedade PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contém um caminho totalmente qualificado que identifica o anexo aos destinatários com acesso a um servidor de arquivos comum. 
    
ATTACH_BY_REF_RESOLVE 
  
> A **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo. 
    
ATTACH_BY_REF_ONLY 
  
> A **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo. 
    
ATTACH_EMBEDDED_MSG 
  
> A **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contém um objeto incorporado que oferece suporte à interface **IMessage.** 
    
ATTACH_OLE 
  
> O anexo é um objeto OLE incorporado.
    
ATTACH_BY_WEBREFERENCE 
  
> O conteúdo do anexo não está na mensagem. 
    
Quando criado, todos os objetos de anexo têm um **valor PR_ATTACH_METHOD** inicial **de NO_ATTACHMENT**. 
  
Aplicativos cliente e provedores de serviços são necessários apenas para dar suporte ao método de anexo representado pelo **ATTACH_BY_VALUE** valor. Os outros métodos de anexo são opcionais. O armazenamento de mensagens não impõe qualquer consistência entre o valor **de PR_ATTACH_METHOD** e os valores das outras propriedades de anexo. 
  
Os nomes UNC são recomendados para caminhos totalmente qualificados,  que devem ser usados com ATTACH_BY_REFERENCE e **ATTACH_BY_REF_ONLY**. Com **ATTACH_BY_REF_RESOLVE**, um caminho absoluto é mais rápido, porque o spooler MAPI converte o anexo em **ATTACH_BY_VALUE**. 
  
Se **ATTACH_BY_REFERENCE** estiver definido, **PR_ATTACH_DATA_BIN** deve estar vazio. Um gateway de saída pode transformar um **ATTACH_BY_REFERENCE** anexo em um anexo **ATTACH_BY_VALUE,** copiando os dados do anexo para a PR_ATTACH_DATA_BIN **propriedade.** 
  
Se **ATTACH_BY_REF_RESOLVE** estiver definido, **PR_ATTACH_DATA_BIN** deve estar vazio. Quando a mensagem que contém o **ATTACH_BY_REF_RESOLVE** anexo é **enviada,** o spooler MAPI copia os dados do anexo em um ATTACH_BY_VALUE anexo. Esse processo de resolução coloca os dados do anexo **PR_ATTACH_DATA_BIN**. 
  
Se **ATTACH_BY_REF_ONLY** for definido, **PR_ATTACH_DATA_BIN** deverá estar vazio e o sistema de mensagens nunca resolverá a referência de anexo. Use esse valor quando quiser enviar o link, mas não os dados. 
  
Quando o objeto OLE está no formato OLE 2.0 **IStorage,** os dados são acessíveis por meio **de PR_ATTACH_DATA_OBJ**. Quando o objeto OLE está no formato OLE 1.0 **OLESTREAM,** os dados são acessíveis por meio PR_ATTACH_DATA_BIN **como** **um IStream**. O tipo de codificação OLE pode ser determinado pelo valor **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para obter mais informações sobre interfaces e formatos OLE, consulte a *Referência do programador OLE.* 
  
## <a name="remarks"></a>Comentários

Quando o **PR_ATTACH_METHOD** é **ATTACH_BY_WEBREFERENCE**, o conteúdo do anexo não está na mensagem. Em vez disso, **PR_ATTACH_LONG_FILENAME** propriedade contém uma URL absoluta para o conteúdo do anexo, que é armazenado online. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

