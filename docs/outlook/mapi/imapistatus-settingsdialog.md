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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439727"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe uma folha de propriedades que permite ao usuário alterar a configuração de um provedor de serviços Esse método não é suportado em objetos de status que o MAPI implementa.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai da folha de propriedades de configuração.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a exibição da folha de propriedades. O sinalizador a seguir pode ser definido:
    
UI_READONLY 
  
> Sugere que o provedor não deve permitir que os usuários alterem as propriedades de configuração. Esse sinalizador é apenas uma sugestão; ela pode ser ignorada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A folha de propriedades de configuração foi exibida com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O objeto de status não dá suporte a esse método, conforme indicado pela ausência do sinalizador STATUS_SETTINGS_DIALOG na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Comentários

O **método IMAPIStatus::SettingsDialog** exibe uma folha de propriedades de configuração. Todos os provedores de serviços devem dar suporte **ao método SettingsDialog,** mas isso não é necessário. Os provedores de serviços podem implementar suas próprias folhas de propriedades ou usar a implementação fornecida no [método IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) do objeto de suporte. **DoConfigPropsheet** cria uma folha de propriedades de leitura/gravação. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se um provedor de transporte remoto tiver configurações, ele deverá fazer o seguinte:
  
- Abra a seção de perfil do provedor de transporte.
    
- Obter as configurações de propriedade do provedor de transporte do perfil.
    
- Exibe as configurações de propriedade em uma caixa de diálogo.
    
- Se a caixa de diálogo permitir a edição das configurações de propriedade, verifique se as novas configurações são válidas e armazene-as novamente na seção de perfil do provedor de transporte.
    
- Retornar S_OK ou qualquer valor de erro retornado durante as etapas anteriores.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a folha de propriedades exibida por **meio de SettingsDialog** para executar várias tarefas, como as seguintes: 
  
- Especifique um armazenamento de mensagens padrão.
    
- Especifique um pedido de transporte.
    
- Especifique um contêiner de agendamento de endereço padrão para navegação.
    
- Especifique uma ordem de pesquisa para resolver nomes ambíguos.
    
- Especifique um livro de endereços pessoal padrão.
    
Os provedores de serviços podem implementar folhas de propriedades de leitura/gravação, somente leitura ou uma combinação de permissões, dependendo da propriedade. Os provedores de serviços podem implementar permissões diferentes em propriedades individuais definindo restrições de propriedade. O modo padrão para folhas de propriedades é leitura/gravação. Você pode solicitar folhas de propriedades somente leitura definindo o sinalizador UI_READONLY em suas chamadas para **SettingsDialog**. Os provedores de serviços que são capazes de implementar folhas de propriedades somente leitura podem fazer isso. No entanto, como alguns provedores de serviços não podem substituir o modo padrão, você deve estar preparado para lidar com folhas de propriedade de qualquer tipo. 
  
Como uma interface do usuário está sempre envolvida nessa operação, somente clientes interativos devem chamar **SettingsDialog**.
  
## <a name="see-also"></a>Confira também



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

