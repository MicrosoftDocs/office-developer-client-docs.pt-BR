---
title: Propriedade canônica PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400254"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propriedade canônica PidTagContainerClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres de texto descrevendo o tipo de uma pasta. Embora esta propriedade é ignorada em geral, as versões do Microsoft® Exchange Server antes do Gerenciador de caixa de correio do Exchange Server 2003 esperam essa propriedade estar presentes.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificador:  <br/> |0x3613  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentários

Normalmente, essas propriedades não são usadas pelo Exchange Server. No entanto, Microsoft Office Outlook® anexa-los às pastas de caixa de correio. Além disso, as versões do Exchange Server antes do Gerenciador de caixa de correio do Exchange Server 2003 incorretamente podem tratar de pastas que não tenham essas propriedades.
  
Os valores de cadeia de caracteres na tabela a seguir podem ser atribuídas a essas propriedades.
  
|**Valor**|**Conteúdo da pasta**|
|:-----|:-----|
|FALHA DE PÁGINA INVÁLIDA. Compromisso  <br/> |Compromissos  <br/> |
|FALHA DE PÁGINA INVÁLIDA. Contato  <br/> |Contatos  <br/> |
|FALHA DE PÁGINA INVÁLIDA. Diário  <br/> |Entradas de diário do Outlook  <br/> |
|FALHA DE PÁGINA INVÁLIDA. Observação  <br/> |Mensagens de email e notas  <br/> |
|FALHA DE PÁGINA INVÁLIDA. StickyNote  <br/> |Notas Autoadesivas do Outlook  <br/> |
|FALHA DE PÁGINA INVÁLIDA. Tarefa  <br/> |Tarefas do Outlook  <br/> |
   
Para pastas que contêm mensagens de email, essas propriedades devem ser definidas como falha de página inválida. Nota.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

