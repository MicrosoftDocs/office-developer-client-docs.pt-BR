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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767210"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Aplica-se a**: Outlook 
  
Exibe uma folha de propriedades que permite ao usuário alterar a configuração de um provedor de serviços, que esse método não é suportado nos objetos de status que implementa de MAPI.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Uma alça para a janela pai da folha de propriedades de configuração.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a exibição da folha de propriedades. O seguinte sinalizador pode ser definido:
    
UI_READONLY 
  
> Sugere que o provedor não deve habilitar os usuários alterem as propriedades de configuração. Esse sinalizador é apenas uma sugestão; pode ser ignorado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A folha de propriedades de configuração foi exibida com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não suporta este método, conforme indicado pela ausência do sinalizador STATUS_SETTINGS_DIALOG na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Comentários

O método **IMAPIStatus:: SettingsDialog** exibe uma folha de propriedades de configuração. Todos os provedores de serviço devem oferecer suporte para o método **SettingsDialog** , mas ela não é necessária. Provedores de serviço podem implementar suas próprias folhas de propriedade ou use a implementação fornecida no método de [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) de suporte do objeto. **DoConfigPropsheet** constrói uma folha de propriedades de leitura/gravação. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se um provedor de transporte remoto tiver quaisquer configurações, ele deve fazer o seguinte:
  
- Abra a seção de perfil do provedor de transporte.
    
- Obtenha o transporte configurações de propriedade do provedor do perfil.
    
- Exiba as configurações de propriedade em uma caixa de diálogo.
    
- Se a caixa de diálogo permite a edição das configurações de propriedade, verifique se as novas configurações são válidas e armazená-los novamente na seção de perfil do provedor de transporte.
    
- Retorne S_OK ou quaisquer valores de erro retornados durante as etapas anteriores.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a folha de propriedades exibida por meio de **SettingsDialog** para realizar várias tarefas, como o seguinte: 
  
- Especifique um armazenamento de mensagens padrão.
    
- Especifica uma ordem de transporte.
    
- Especifique um contêiner de catálogo de endereços padrão para navegação.
    
- Especifica uma ordem de pesquisa para resolução de nomes ambíguos.
    
- Especifique um catálogo de endereços pessoal padrão.
    
Provedores de serviço podem implementar folhas de propriedades que são de leitura/gravação, somente leitura, ou uma mistura de permissões, dependendo da propriedade. Provedores de serviços podem implementar diferentes permissões nas propriedades individuais, definindo restrições de propriedade. O modo padrão de folhas de propriedade é leitura/gravação. Você pode solicitar folhas de propriedade somente leitura, definindo o sinalizador UI_READONLY em suas chamadas a **SettingsDialog**. Provedores de serviço podem implementar folhas de propriedade somente leitura podem fazê-lo. No entanto, pois alguns provedores de serviços não podem substituir o modo padrão, você deve ser preparado para lidar com as folhas de propriedades de qualquer tipo. 
  
Como uma interface de usuário é sempre envolvida nesta operação, somente clientes interativos devem chamar **SettingsDialog**.
  
## <a name="see-also"></a>Confira também



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

