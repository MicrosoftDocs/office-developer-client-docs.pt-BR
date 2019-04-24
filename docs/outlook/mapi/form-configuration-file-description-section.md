---
title: Seção do arquivo de configuração de formulários [Descrição]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320983"
---
# <a name="form-configuration-file-description-section"></a>Seção do arquivo de configuração de formulários [Descrição]
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[Descrição]** lista todas as propriedades do formulário que estão associadas aos controles na interface do usuário do formulário, além de atributos usados na localização do formulário. As **** entradas MessageClass, **CLSID**e **DisplayName** , que identificam o nome da classe de mensagem do formulário, seu GUID e o nome de exibição da classe de mensagem, respectivamente, são entradas obrigatórias usadas para localizar o formulário na biblioteca de formulários . As entradas restantes são opcionais. O formato da seção **[Descrição]** é: 
  
A seção **[Descrição]** lista todas as propriedades do formulário que estão associadas aos controles na interface do usuário do formulário, além de atributos usados na localização do formulário. As **** entradas MessageClass, **CLSID**e **DisplayName** , que identificam o nome da classe de mensagem do formulário, seu GUID e o nome de exibição da classe de mensagem, respectivamente, são entradas obrigatórias usadas para localizar o formulário na biblioteca de formulários . As entradas restantes são opcionais. O formato da seção **[Descrição]** é: 
  
 **Descrição ** =  _Cadeia de caracteres_ MessageClass
  
 **** =  _GUID_ do CLSID
  
 **DisplayName** =  __ disjogadostring
  
 **** =  _Caminho_ de SmallIcon
  
 **** =  _Caminho_ LargeIcon
  
As entradas opcionais são:
  
 **** =  _Cadeia de caracteres exibida_ na categoria
  
 **** =  _Cadeia de caracteres exibida_ na subcategoria
  
 **** =  _Cadeia de caracteres exibida_ de comentário
  
 **** =  _Cadeia de caracteres exibida_ do proprietário
  
 **** =  _Cadeia de caracteres exibida_ de número
  
 **** =  _Inteiro_ de versão
  
 **** =  _Cadeia de caracteres_ de localidade
  
 **** =  _Inteiro_ oculto
  
 **** =  _Cadeia de caracteres_ DesignerToolName
  
 **DesignerToolGuid** =  _CLSID_
  
 **DesignerRuntimeGuid** =  _CLSID_
  
 **ComposeInFolder** =  _0 | 1_
  
 **** =  _Cadeia de caracteres_ ComposeCommand
  
As entradas de **categoria** e de subcategoria são usadas por instaladores de formulário para configurar a categorização padrão de formulários dentro da interface do usuário do aplicativo cliente. **** Por exemplo, uma hierarquia pode ser configurada onde "Help Desk" é a categoria e "software" e "hardware" foram as subcategorias. Essa categorização pode ser usada por aplicativos de visualização para exibir mensagens de uma maneira mais organizada. As entradas de **Comentário**, **proprietário**e **número** são todas as cadeias de caracteres de comentário que aparecem na interface de usuário do aplicativo cliente. São propriedades específicas de formulário que podem ser usadas com a critério do desenvolvedor de formulários. Por exemplo, a entrada de **Comentário** pode ser usada para indicar a finalidade do formulário, a entrada do **proprietário** usada para indicar a pessoa ou organização responsável por manter o formulário e o número usado para controlar a versão diferente do formulário. Para a entrada de **Comentário** , podem ser incluídas até dez linhas de comentários. A primeira linha de comentários usa a palavra "Comment" como a chave, a segunda linha de comentários usa "Comment1" como a chave e assim por diante por meio de "Comment9". 
  
As entradas **LargeIcon** e **SmallIcon** são usadas para especificar o caminho dos recursos de ícone usados para exibir ícones na interface de usuário do aplicativo cliente, geralmente é para linhas de tabela que incluem o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Os nomes de arquivos de ícone podem ser especificados como caminhos relativos ao diretório onde o arquivo de configuração de formulário está instalado. A entrada de **versão** é usada para indicar o número de versão do formulário. **Locale** é o identificador de idioma de três letras da biblioteca de formulários de destino. Uma lista desses identificadores pode ser encontrada na _referência do programador do Win32_.
  
A entrada **Hidden** indica se o formulário deve ser exibido na interface de usuário de um provedor de biblioteca de formulários: 1 indica que o arquivo está oculto e 0 indica que o formulário está visível. Um exemplo de arquivo de configuração de formulário é mostrado a seguir. 
  
A entrada **ComposeInFolder** controla se o formulário foi projetado para ser colocado na pasta atual ou na caixa de entrada do usuário quando o usuário salvar a mensagem ao redigi-la: 1 indica que o formulário deve ir na pasta atual e 0 indica que ele deve Vá na caixa de entrada. 
  
A entrada **ComposeCommand** é a cadeia de caracteres a ser colocada no menu de redação do aplicativo cliente. Se isso não for especificado, a entrada **DisplayName** será usada. 
  
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


