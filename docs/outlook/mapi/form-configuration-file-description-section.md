---
title: Seção de [descrição] do arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d3673c3b10afb55121339e335163ce9b2e5937e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766578"
---
# <a name="form-configuration-file-description-section"></a>Seção de [descrição] do arquivo de configuração de formulário
 
**Aplica-se a**: Outlook 
  
A seção **[descrição]** lista todas as propriedades do formulário que estão associadas a controles de interface do usuário, mais atributos que são usados na localização de formulário do formulário. O **MessageClass**, **Clsid**e entradas de **DisplayName** , que identificam o nome de classe de mensagem do formulário, seu GUID e nome de exibição da classe de mensagem, respectivamente, são entradas necessárias usadas para localizar o formulário dentro da biblioteca de formulário . As entradas restantes são opcionais. O formato da seção **[descrição]** é: 
  
A seção **[descrição]** lista todas as propriedades do formulário que estão associadas a controles de interface do usuário, mais atributos que são usados na localização de formulário do formulário. O **MessageClass**, **Clsid**e entradas de **DisplayName** , que identificam o nome de classe de mensagem do formulário, seu GUID e nome de exibição da classe de mensagem, respectivamente, são entradas necessárias usadas para localizar o formulário dentro da biblioteca de formulário . As entradas restantes são opcionais. O formato da seção **[descrição]** é: 
  
 **[Descrição] MessageClass** =  _cadeia de caracteres_
  
 **CLSID** =  _guid_
  
 **DisplayName** =  _displayedstring_
  
 **SmallIcon** =  _caminho_
  
 **LargeIcon** =  _caminho_
  
Entradas opcionais são:
  
 **Categoria** =  _exibido a cadeia de caracteres_
  
 **Subcategoria** =  _exibido a cadeia de caracteres_
  
 **Comentário** =  _exibido a cadeia de caracteres_
  
 **Proprietário** =  _exibido a cadeia de caracteres_
  
 **Número** =  _exibido a cadeia de caracteres_
  
 **Versão** =  _inteiro_
  
 **Localidade** =  _cadeia de caracteres_
  
 **Oculto** =  _inteiro_
  
 **DesignerToolName** =  _cadeia de caracteres_
  
 **DesignerToolGuid** =  _clsid_
  
 **DesignerRuntimeGuid** =  _clsid_
  
 **ComposeInFolder** =  _0 | 1_
  
 **ComposeCommand** =  _cadeia de caracteres_
  
As entradas de **categoria** e uma **subcategoria** são usadas pelo instaladores de formulário para configurar a categorização de padrão de formulários dentro da interface do usuário do aplicativo cliente. Por exemplo, uma hierarquia pode ser configurada tal onde "Help Desk" é a categoria e "Software" e "Hardware" eram as subcategorias. Esta categorização, em seguida, pode ser usada por aplicativos de visualizador para exibir mensagens de uma maneira mais organizada. As entradas de **comentário**, **proprietário**e **número** são todas as cadeias de caracteres de comentário que aparecem na interface do usuário do aplicativo cliente. Estas são as propriedades específicas de formulário que podem ser usadas a critério do desenvolvedor do formulário. Por exemplo, a entrada de **comentário** pode ser usada para indicar a finalidade do formulário, a entrada do **proprietário** usada para indicar a pessoa ou organização responsável por manter o formulário e o número usado para rastrear uma versão diferente do formulário. Para o **comentário** de entrada, até dez linhas de comentários pode ser incluída. A primeira linha de comentários usa a palavra "Comentário" como a chave, a segunda linha de comentários usa "Comment1" como a chave, e assim por diante por meio de "Comment9". 
  
As entradas **LargeIcon** e **SmallIcon** são usadas para especificar o caminho para os recursos de ícone usado para exibir ícones na interface de usuário do aplicativo cliente, que normalmente é para linhas de tabela que incluem **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou colunas de propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Nomes de arquivo de ícone podem ser especificados como nomes de caminho relativo para o diretório onde o arquivo de configuração do formulário está instalado. A entrada de **versão** é usada para indicar o número da versão do formulário. **Locale** é o identificador de idioma de três letras da biblioteca de formulários de destino. Uma lista desses identificadores pode ser encontrada na _referência do programador do Win32_.
  
A entrada de **oculto** indica se o formulário deve ser exibido na interface do usuário de um provedor biblioteca de formulário: 1 indica que o arquivo está oculto e 0 indica que o formulário está visível. Um arquivo de configuração do formulário de exemplo é mostrado a seguir. 
  
A entrada **ComposeInFolder** controla se o formulário foi projetado para ser colocado na pasta atual ou na caixa de entrada do usuário quando o usuário salva a mensagem enquanto escrevendo: 1 indica que o formulário deve ir na pasta atual e 0 indica que ele deve vá na caixa de entrada. 
  
A entrada **ComposeCommand** é a cadeia de caracteres sejam colocadas no aplicativo cliente do menu redigir. Se não for especificado, a entrada **DisplayName** será usada. 
  
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


