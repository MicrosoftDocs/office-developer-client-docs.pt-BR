---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430571"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra o spooler MAPI em um armazenamento de mensagens.
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>Parâmetros

 _lpMAPISup_
  
> [in] Um ponteiro para o objeto de suporte MAPI para o armazenamento de mensagens.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. 
    
 _lpszProfileName_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para o logon do spooler MAPI. Essa cadeia de caracteres pode ser exibida em caixas de diálogo, escritas em um arquivo de log ou simplesmente ignoradas. Ele deverá estar no formato Unicode se o sinalizador MAPI_UNICODE estiver definido no _parâmetro ulFlags._ 
    
 _cbEntryID_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para o armazenamento de mensagens. Passar NULL no parâmetro  _lpEntryID_ indica que um armazenamento de mensagens ainda não foi selecionado e que caixas de diálogo que permitem ao usuário selecionar um armazenamento de mensagens podem ser apresentadas. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o logon é realizado. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> A chamada tem permissão para ser bem-sucedida, mesmo se o objeto subjacente não estiver disponível para a implementação da chamada. Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá criar um erro.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
MDB_NO_DIALOG 
  
> Impede a exibição de caixas de diálogo de logon. Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED será retornado se o logon não for bem-sucedido. Se esse sinalizador não estiver definido, o provedor do armazenamento de mensagens poderá solicitar que o usuário corrija um nome ou senha, insira um disco ou execute outras ações necessárias para estabelecer conexão com o armazenamento.
    
MDB_WRITE 
  
> Solicita permissão de leitura/gravação.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador da interface) para o armazenamento de mensagens fazer logon. Passar NULL indica que a interface MAPI do repositório de mensagens ([IMsgStore](imsgstoreimapiprop.md)) é retornada. O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o armazenamento de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Um ponteiro para o tamanho, em bytes, dos dados de validação no _parâmetro lppbSpoolSecurity._ 
    
 _lpbSpoolSecurity_
  
> [in] Um ponteiro para um ponteiro para dados de validação. O **método SpoolerLogon** usa esses dados para fazer logon do spooler MAPI no mesmo armazenamento que o provedor de armazenamento de mensagens conectado anteriormente usando o método [IMSProvider::Logon.](imsprovider-logon.md) 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura [MAPIERROR](mapierror.md) retornada, se alguma, que contenha informações de versão, componente e contexto para um erro. O  _parâmetro lppMAPIError_ pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada. 
    
 _lppMSLogon_
  
> [out] Um ponteiro para o ponteiro para o objeto de logon do armazenamento de mensagens para MAPI fazer logon.
    
 _lppMDB_
  
> [out] Um ponteiro para o ponteiro para o objeto de armazenamento de mensagens para o spooler MAPI e aplicativos cliente para fazer logoff.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_UNCONFIGURED 
  
> O perfil não contém informações suficientes para que o logon seja concluído. Quando esse valor é retornado, o MAPI chama a função de ponto de entrada do serviço de mensagens do provedor de armazenamento de mensagens.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas o provedor do armazenamento de mensagens tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md) Para obter as informações de erro do provedor, chame o [método IMAPISession::GetLastError.](imapisession-getlasterror.md) 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o **método IMSProvider::SpoolerLogon** para fazer logoff em um armazenamento de mensagens. O spooler MAPI deve usar o objeto de armazenamento de mensagens retornado pelo provedor de armazenamento de mensagens no parâmetro  _lppMDB_ durante e após o logon. 
  
Para consistência com o [método IMSProvider::Logon,](imsprovider-logon.md) o provedor também retorna um objeto de logon do armazenamento de mensagens no parâmetro _lppMSLogon._ O uso do objeto de armazenamento e do objeto de logon são idênticos para logon de armazenamento normal; deve haver uma correspondência um-para-um entre o objeto de logon e o objeto de armazenamento de forma que os objetos agem como se fosse um objeto que expõe duas interfaces. Os dois objetos são criados juntos e liberados juntos. 
  
O provedor de armazenamento deve marcar internamente o objeto de armazenamento de mensagens retornado para indicar que o armazenamento está sendo usado pelo spooler MAPI. Alguns dos métodos para esse objeto de armazenamento se comportam de maneira diferente do objeto de armazenamento de mensagens fornecido aos aplicativos cliente. Manter essa marca interna é a maneira mais comum de disparar o comportamento específico para o spooler MAPI.
  
## <a name="see-also"></a>Confira também



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

