---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405083"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Instala um formulário em uma biblioteca de formulários.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O parâmetro _ulUIParam_ é ignorado, a menos que o aplicativo cliente defina o sinalizador MAPI_DIALOG no parâmetro _parâmetroulflags_ . O parâmetro _ulUIParam_ pode ser nulo se MAPI_DIALOG também não for passado. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla a instalação do formulário. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo para fornecer informações de progresso ou solicitar mais informações ao usuário. Se esse sinalizador não for definido, nenhuma caixa de diálogo será exibida.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Se já existir outro formulário que manipule a classe de mensagens manipulada por este formulário, substitua o formulário existente por este. Este sinalizador será ignorado se o sinalizador MAPI_DIALOG também estiver presente. 
    
 _szCfgPathName_
  
> no O caminho para o arquivo de configuração do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_EXTENDED_ERROR 
  
> Ocorreu um erro de implementação. Para obter a estrutura [MAPIERROR](mapierror.md) associada ao erro, chame o método [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a instalação do formulário, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Os provedores de biblioteca de formulários devem preencher uma estrutura **MAPIERROR** e retornar MAPI_E_EXTENDED_ERROR se qualquer uma das seguintes condições ocorrer: 
  
- O arquivo de configuração não foi encontrado.
    
- O arquivo de configuração não é legível.
    
- O arquivo de configuração é inválido.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Os aplicativos cliente chamam o método **IMAPIFormContainer:: InstallForm** para instalar um formulário em um contêiner de formulário específico. O parâmetro _szCfgPathName_ deve conter o caminho de um arquivo de configuração de formulário (ou seja, um arquivo com a extensão. cfg que descreve o formulário e sua implementação). Os sinalizadores no parâmetro _parâmetroulflags_ especificam o seguinte: 
  
- Se o sinalizador MAPI_DIALOG estiver definido, uma interface do usuário será exibida, permitindo que o usuário que está instalando o formulário especifique os detalhes da instalação.
    
- Se o sinalizador MAPIFORM_INSTALL_OVERWRITEONCONFLICT estiver definido, qualquer formulário anterior para a mesma classe de mensagem será substituído pelo formulário que está sendo instalado. Caso contrário, a instalação do formulário será mesclada com a descrição do formulário atual, se houver uma.
    
- Se MAPI_DIALOG for definido, MAPIFORM_INSTALL_OVERWRITEONCONFLICT será ignorada.
    
- A ausência de MAPIFORM_INSTALL_OVERWRITEONCONFLICT no sinalizador definido significa que uma mesclagem será feita. Quaisquer plataformas novas no arquivo. cfg que não estejam atualmente presentes na descrição do formulário serão instaladas e nenhuma outra alteração ocorrerá.
    
- Se o sinalizador MAPI_UNICODE estiver definido, o caminho do arquivo de configuração de formulário será uma cadeia de caracteres Unicode. 
    
Os clientes devem chamar [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) se **InstallForm** retornar MAPI_E_EXTENDED_ERROR e deve verificar a estrutura de [MAPIERROR](mapierror.md) retornada para determinar a condição que gerou o erro. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnInstallForm  <br/> |MFCMAPI usa o método **IMAPIFormContainer:: InstallForm** para instalar um formulário em um contêiner de formulários.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

