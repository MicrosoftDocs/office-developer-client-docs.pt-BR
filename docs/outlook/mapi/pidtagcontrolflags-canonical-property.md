---
title: Propriedade canônica PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769130"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propriedade canônica PidTagControlFlags

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos sinalizadores que controlam o comportamento de um controle usado em uma caixa de diálogo construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificador:  <br/> |0x3F00  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabela de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade:
  
DT_ACCEPT_DBCS 
  
> O controle pode ter caracteres do conjunto de caracteres de Byte duplo (DBCS) nela. Esse sinalizador é usado com controles de edição. Ele permite que os conjuntos de caracteres de vários bytes.
    
DT_EDITABLE 
  
> O controle pode ser editado; o valor associado ao controle pode ser alterado. Quando esse sinalizador não estiver definida, o controle é somente leitura. Este valor será ignorado no rótulo, caixa de grupo, botão de ação padrão, suspenso multivalorado de caixa de listagem e controles de caixa de lista.
    
DT_MULTILINE 
  
> O controle de edição pode conter várias linhas. Isso significa que um caractere de retorno pode ser digitado dentro do controle. Esse sinalizador é válida para apenas controles de edição.
    
DT_PASSWORD_EDIT 
  
> Aplica-se para editar os controles. O controle de edição é tratado como uma senha. O valor é exibido usando asteriscos em vez de ecos os caracteres reais inseridos.
    
DT_REQUIRED 
  
> Se o controle permitir alterações (DT_EDITABLE), ele deve ter um valor antes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado. 
    
DT_SET_IMMEDIATE 
  
> Permite a configuração imediata de um valor; Assim que um valor no controle é alterado, MAPI chama o método **SetProps** para a propriedade associada a esse controle. Quando esse sinalizador não estiver definida, os valores são definidos quando a caixa de diálogo é descartada. 
    
DT_SET_SELECTION 
  
> Quando uma seleção é feita na caixa de lista, a coluna de índice da caixa de listagem é definida como uma propriedade. Sempre é usado com DT_SET_IMMEDIATE.
    
Essa propriedade é armazenada no membro ulCtlFlags da estrutura [DTCTL](dtctl.md) de um controle. A maioria dos sinalizadores controle se aplicam a todos os controles que permitem a entrada do usuário; Alguns se aplicam apenas ao controle de edição. Controles que não permitem a entrada de usuário, um botão ou um rótulo, defina 0 para seus sinalizadores de controle. 
  
Muitos dos valores sinalizador são auto-explicativos. Por exemplo, quando DT_REQUIRED é definida para um controle, ele deve conter um valor antes que a caixa de diálogo tem permissão para ser descartado. O provedor de serviços pode fornecer um valor pela sua implementação **IMAPIProp** ou o usuário pode digitar um. DT_EDITABLE indica que o valor do controle pode ser modificado. DT_MULTILINE permite que o valor de um controle de edição abranger várias linhas. 
  
Alguns sinalizadores de controle não são tão óbvias no seu significado. Quando um controle define o sinalizador DT_SET_IMMEDIATE, todas as alterações feitas take seu valor afetam assim que o usuário move para um novo controle. MAPI torna uma única chamada de método de [IMAPIProp::SetProps](imapiprop-setprops.md) da interface de propriedade para a propriedade do controle. Isso é diferente do comportamento padrão, que é para adiar tendo alterações nos valores de controle entrarão em vigor depois que o usuário seleciona o botão **Okey** ou descarte a caixa de diálogo. O sinalizador DT_SET_IMMEDIATE é frequentemente usado em combinação com notificações de tabela de exibição. 
  
A tabela a seguir lista os tipos de controles e todos os valores de sinalizador que podem ser definidos para cada tipo.
  
|**Control**|**Valores válidos para esta propriedade**|
|:-----|:-----|
|Botão  <br/> |Deve ser zero  <br/> |
|Caixa de seleção  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Caixa de combinação  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Caixa de listagem drop-down  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|EDIT  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Caixa de grupo  <br/> |Deve ser zero  <br/> |
|Rótulo  <br/> |Deve ser zero  <br/> |
|Caixa de listagem  <br/> |Deve ser zero  <br/> |
|Caixa de listagem de lista suspensa de vários valores  <br/> |Deve ser zero  <br/> |
|Caixa de listagem de vários valores  <br/> |Deve ser zero  <br/> |
|Página com guias  <br/> |Deve ser zero  <br/> |
|Botão de opção  <br/> |Deve ser zero  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

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

