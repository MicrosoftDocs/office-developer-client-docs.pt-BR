---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331539"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe uma folha de propriedades que permite que o usuário altere a configuração de um provedor de serviços esse método não tem suporte nos objetos de status que o MAPI implementa.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai da folha de propriedades de configuração.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla a exibição da folha de propriedades. O seguinte sinalizador pode ser definido:
    
UI_READONLY 
  
> Sugere que o provedor não deve permitir que os usuários alterem as propriedades de configuração. Este sinalizador é apenas uma sugestão; pode ser ignorado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A folha de propriedades de configuração foi exibida com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não oferece suporte a esse método, conforme indicado pela ausência do sinalizador STATUS_SETTINGS_DIALOG na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Comentários

O método **IMAPIStatus:: SettingsDialog** exibe uma folha de propriedades de configuração. Todos os provedores de serviços devem oferecer suporte ao método **SettingsDialog** , mas não são necessários. Os provedores de serviços podem implementar suas próprias folhas de propriedades ou usar a implementação fornecida no método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) do objeto support. **DoConfigPropsheet** cria uma folha de propriedades de leitura/gravação. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se um provedor de transporte remoto tiver configurações, deverá fazer o seguinte:
  
- Abra a seção perfil do provedor de transporte.
    
- Obtenha as configurações de Propriedade do provedor de transporte do perfil.
    
- Exibe as configurações de propriedade em uma caixa de diálogo.
    
- Se a caixa de diálogo permitir a edição das configurações de propriedade, verifique se as novas configurações são válidas e armazene-as novamente na seção perfil do provedor de transporte.
    
- Retorna S_OK ou qualquer valor de erro retornado durante as etapas anteriores.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a folha de propriedades exibida através do **SettingsDialog** para executar várias tarefas, como as seguintes: 
  
- Especifique um repositório de mensagens padrão.
    
- Especifique uma ordem de transporte.
    
- Especifique um contêiner de catálogo de endereços padrão para navegação.
    
- Especifique uma ordem de pesquisa para resolver nomes ambíguos.
    
- Especifique um catálogo de endereços pessoal padrão.
    
Os provedores de serviços podem implementar folhas de propriedades que são leitura/gravação, somente leitura ou uma mistura de permissões, dependendo da propriedade. Os provedores de serviços podem implementar diferentes permissões em propriedades individuais definindo restrições de propriedade. O modo padrão para folhas de propriedades é leitura/gravação. Você pode solicitar folhas de propriedades somente leitura Configurando o sinalizador UI_READONLY em suas chamadas para **SettingsDialog**. Provedores de serviços capazes de implementar folhas de propriedades somente leitura podem fazê-lo. No enTanto, como alguns provedores de serviços não podem substituir o modo padrão, você deve estar preparado para lidar com as folhas de propriedades de qualquer tipo. 
  
Como uma interface do usuário está sempre envolvida nesta operação, somente os clientes interativos devem chamar **SettingsDialog**.
  
## <a name="see-also"></a>Confira também



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

