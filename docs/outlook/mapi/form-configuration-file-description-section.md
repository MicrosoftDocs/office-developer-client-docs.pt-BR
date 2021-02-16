---
title: Seção Arquivo de Configuração do Formulário [Descrição]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433091"
---
# <a name="form-configuration-file-description-section"></a>Seção Arquivo de Configuração do Formulário [Descrição]
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Descrição]** lista todas as propriedades do formulário que estão associadas a controles na interface do usuário do formulário, além de atributos usados na localização do formulário. As entradas **MessageClass**, **Clsid** e **DisplayName,** que identificam o nome da classe de mensagem do formulário, seu GUID e o nome de exibição da classe de mensagem, respectivamente, são entradas necessárias usadas para localizar o formulário dentro da biblioteca de formulário. As entradas restantes são opcionais. O formato da **seção [Descrição]** é: 
  
A **seção [Descrição]** lista todas as propriedades do formulário que estão associadas a controles na interface do usuário do formulário, além de atributos usados na localização do formulário. As entradas **MessageClass**, **Clsid** e **DisplayName,** que identificam o nome da classe de mensagem do formulário, seu GUID e o nome de exibição da classe de mensagem, respectivamente, são entradas necessárias usadas para localizar o formulário dentro da biblioteca de formulário. As entradas restantes são opcionais. O formato da **seção [Descrição]** é: 
  
 **[Description] MessageClass**  =   _string_
  
 **Clsid**  =   _guid_
  
 **DisplayName**  =   _displayedstring_
  
 **SmallIcon**  =   _path_
  
 **LargeIcon**  =   _path_
  
As entradas opcionais são:
  
 **Categoria**  =   _cadeia de caracteres exibida_
  
 **Subcategoria**  =   _cadeia de caracteres exibida_
  
 **Comentário**  =   _cadeia de caracteres exibida_
  
 **Proprietário**  =   _cadeia de caracteres exibida_
  
 **Número**  =   _cadeia de caracteres exibida_
  
 **Versão**  =   _integer_
  
 **Localidade**  =   _string_
  
 **Oculto**  =   _integer_
  
 **DesignerToolName**  =   _string_
  
 **DesignerToolGuid**  =   _clsid_
  
 **DesignerRuntimeGuid**  =   _clsid_
  
 **ComposeInFolder**  =   _0|1_
  
 **ComposeCommand**  =   _string_
  
As **entradas Categoria** e **Subcategoria** são usadas por instaladores de formulário para configurar a categorização padrão de formulários na interface do usuário do aplicativo cliente. Por exemplo, uma hierarquia poderia ser configurada onde "Help Desk" é a categoria e "Software" e "Hardware" eram as subcategorias. Essa categorização pode ser usada pelos aplicativos de visualização para exibir mensagens de maneira mais organizada. As **entradas Comment**, **Owner** e **Number** são todas as cadeias de caracteres de comentário que aparecem na interface do usuário do aplicativo cliente. Estas são propriedades específicas do formulário que podem ser usadas a critério do desenvolvedor do formulário. For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form. Para a **entrada Comentário,** até dez linhas de comentários podem ser incluídas. A primeira linha de comentários usa a palavra "Comment" como a chave, a segunda linha de comentários usa "Comment1" como a chave e assim por diante através de "Comment9". 
  
As entradas **LargeIcon** e **SmallIcon** são usadas para especificar o caminho para os recursos de ícone usados para exibir ícones na interface do usuário do aplicativo cliente, normalmente isso se aplica a linhas de tabela que incluem as colunas de propriedade **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Os nomes de arquivo de ícone podem ser especificados como nomes de caminho relativos ao diretório onde o arquivo de configuração de formulário está instalado. A **entrada** version é usada para indicar o número de versão do formulário. **Localidade é** o identificador de idioma de três letras da biblioteca de formulário de destino. Uma lista desses identificadores pode ser encontrada na Referência do programador _do Win32._
  
A **entrada** Oculta indica se o formulário deve ser exibido na interface do usuário de um provedor de biblioteca de formulário: 1 indica que o arquivo está oculto e 0 indica que o formulário está visível. Um exemplo de arquivo de configuração de formulário é mostrado a seguir. 
  
A entrada **ComposeInFolder** controla se o formulário foi projetado para ser colocado na pasta atual ou na Caixa de Entrada do usuário quando o usuário salva a mensagem enquanto a compõe: 1 indica que o formulário deve ir para a pasta atual e 0 indica que ele deve ir para a Caixa de Entrada. 
  
A **entrada ComposeCommand** é a cadeia de caracteres a ser colocada no menu de redação do aplicativo cliente. Se isso não for especificado, a **entrada DisplayName** será usada. 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


