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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283146"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propriedade canônica PidTagContainerClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres de texto que descreve o tipo de uma pasta. Embora essa propriedade seja geralmente ignorada, as versões do Microsoft® Exchange Server anteriores ao Gerenciador de Caixa de Correio do Exchange Server 2003 esperam que essa propriedade estará presente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificador:  <br/> |0x3613  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Contêiner  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades normalmente não são usadas pelo Exchange Server. No entanto, o Microsoft Office Outlook ® anexa-os a pastas de caixa de correio. Além disso, as versões do Exchange Server anteriores ao Gerenciador de Caixa de Correio do Exchange Server 2003 podem lidar incorretamente com pastas que não têm essas propriedades.
  
Essas propriedades podem ser atribuídas aos valores de cadeia de caracteres na tabela a seguir.
  
|**Valor**|**Conteúdo da pasta**|
|:-----|:-----|
|IPF. Compromisso  <br/> |Compromissos  <br/> |
|IPF. Contato  <br/> |Contatos  <br/> |
|IPF. Diário  <br/> |Entradas de Diário do Outlook  <br/> |
|IPF. Observação  <br/> |Mensagens de Email e anotações  <br/> |
|IPF. StickyNote  <br/> |Observações Desaderentadas do Outlook  <br/> |
|IPF. Tarefa  <br/> |Tarefas do Outlook  <br/> |
   
Para pastas que contêm mensagens de email, essas propriedades devem ser definidas como IPF. Observação.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e objetos de lista de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

