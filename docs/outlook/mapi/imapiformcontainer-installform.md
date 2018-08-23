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
ms.openlocfilehash: fd7bc8f051e9584fc63f22bdbaf9696c2e4d15a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580933"
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
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe. O parâmetro _ulUIParam_ é ignorado, a menos que o aplicativo cliente define o sinalizador MAPI_DIALOG no parâmetro _ulFlags_ . O parâmetro _ulUIParam_ pode ser NULL se MAPI_DIALOG também não é passado. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a instalação do formulário. Sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo para fornecer informações sobre o andamento ou solicita ao usuário para obter mais informações. Se esse sinalizador não estiver definida, nenhuma caixa de diálogo é exibida.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Se outro formulário já existir que trata a classe de mensagem manipulada neste formulário, substitua o formulário existente por este. Esse sinalizador é ignorada se o sinalizador MAPI_DIALOG também está presente. 
    
 _szCfgPathName_
  
> [in] O caminho para o arquivo de configuração do formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_EXTENDED_ERROR 
  
> Ocorreu um erro de implementação. Para obter a estrutura [MAPIERROR](mapierror.md) que está associada com o erro, chame o método [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a instalação do formulário, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Provedores de biblioteca de formulário devem preencher uma estrutura **MAPIERROR** e retornar MAPI_E_EXTENDED_ERROR se qualquer uma das seguintes condições ocorrerem: 
  
- O arquivo de configuração não foi encontrado.
    
- O arquivo de configuração não é legível.
    
- O arquivo de configuração é inválido.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Aplicativos cliente chamam o método de **IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário específico. O parâmetro _szCfgPathName_ deve conter o caminho de um arquivo de configuração de formulário (ou seja, um arquivo com a extensão. cfg que descreva o formulário e sua implementação). Os sinalizadores no parâmetro _ulFlags_ especificam o seguinte: 
  
- Se o sinalizador MAPI_DIALOG estiver definido, uma interface do usuário é exibida, permitindo que o usuário que estiver instalando o formulário para especificar detalhes da instalação.
    
- Se o sinalizador MAPIFORM_INSTALL_OVERWRITEONCONFLICT estiver definido, qualquer formato anterior para a mesma classe de mensagem é substituído com o formulário está sendo instalado. Caso contrário, a instalação do formulário é mesclada com a descrição do formulário atual, se houver uma.
    
- Se for definido MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT será ignorada.
    
- A ausência de MAPIFORM_INSTALL_OVERWRITEONCONFLICT na sinalizar defina significa que uma mesclagem será feita. Quaisquer novas plataformas no arquivo. cfg que não estão presentes no momento na descrição do formulário serão instaladas e nenhuma outra alteração ocorrerá.
    
- Se o sinalizador MAPI_UNICODE estiver definido, o caminho do arquivo de configuração de formulário é uma cadeia de caracteres Unicode. 
    
Clientes devem chamar [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) se **InstallForm** retorna MAPI_E_EXTENDED_ERROR, e eles devem verificar a estrutura [MAPIERROR](mapierror.md) retornada para determinar a condição que gerou o erro. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI usa o método **IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

