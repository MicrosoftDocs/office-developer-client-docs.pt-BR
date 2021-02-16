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
  
Instala um formulário em uma biblioteca de formulário.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O _parâmetro ulUIParam é_ ignorado, a menos que o aplicativo cliente defina o MAPI_DIALOG padrão no parâmetro _ulFlags._ O  _parâmetro ulUIParam_ poderá ser NULL se MAPI_DIALOG também for passado. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a instalação do formulário. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo para fornecer informações de progresso ou solicitar ao usuário mais informações. Se esse sinalizador não estiver definido, nenhuma caixa de diálogo será exibida.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> If another form already exists that handles the message class handled by this form, replace the existing form with this one. Esse sinalizador será ignorado se o sinalizador MAPI_DIALOG também estiver presente. 
    
 _szCfgPathName_
  
> [in] O caminho para o arquivo de configuração do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_EXTENDED_ERROR 
  
> Ocorreu um erro de implementação. Para obter a [estrutura MAPIERROR](mapierror.md) associada ao erro, chame o método [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md) 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a instalação do formulário, normalmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Os provedores de biblioteca de formulário devem preencher uma estrutura **MAPIERROR** e retornar MAPI_E_EXTENDED_ERROR caso ocorra uma das seguintes condições: 
  
- O arquivo de configuração não foi encontrado.
    
- O arquivo de configuração não pode ser lido.
    
- O arquivo de configuração é inválido.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Os aplicativos cliente chamam **o método IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário específico. O  _parâmetro szCfgPathName_ deve conter o caminho de um arquivo de configuração de formulário (ou seja, um arquivo com a extensão .cfg que descreve o formulário e sua implementação). Os sinalizadores no  _parâmetro ulFlags_ especificam o seguinte: 
  
- Se o MAPI_DIALOG sinalizador estiver definido, uma interface do usuário será exibida, permitindo que o usuário que está instalando o formulário especifique detalhes de instalação.
    
- Se o MAPIFORM_INSTALL_OVERWRITEONCONFLICT sinalizador estiver definido, qualquer formulário anterior para a mesma classe de mensagem será substituído pelo formulário que está sendo instalado. Caso contrário, a instalação do formulário será mesclada com a descrição do formulário atual, se houver uma.
    
- Se MAPI_DIALOG estiver definido, MAPIFORM_INSTALL_OVERWRITEONCONFLICT será ignorado.
    
- A ausência de MAPIFORM_INSTALL_OVERWRITEONCONFLICT no conjunto de sinalizadores significa que uma mesclagem será feita. Todas as novas plataformas no arquivo .cfg que não estão presentes no momento na descrição do formulário serão instaladas e nenhuma outra alteração ocorrerá.
    
- Se o MAPI_UNICODE padrão estiver definido, o caminho do arquivo de configuração de formulário será uma cadeia de caracteres Unicode. 
    
Os clientes devem chamar [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) se **InstallForm** retornar MAPI_E_EXTENDED_ERROR e eles devem verificar a estrutura [MAPIERROR](mapierror.md) retornada para determinar a condição que gerou o erro. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI usa o **método IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

