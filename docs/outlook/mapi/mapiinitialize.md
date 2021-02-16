---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411173"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Incrementa a contagem de referência do subsistema MAPI e inicializa dados globais para a DLL MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Parâmetros

 _lpMapiInit_
  
> [in] Ponteiro para uma [MAPIINIT_0](mapiinit_0.md) estrutura. O  _parâmetro lpMapiInit_ pode ser definido como NULL. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O subsistema MAPI foi inicializado com êxito.
    
## <a name="remarks"></a>Comentários

A **função MAPIInitialize** incrementa a contagem de referência MAPI para o subsistema MAPI, e a função [MAPIUninitialize](mapiuninitialize.md) diminui a contagem de referência interna. Assim, o número de chamadas para uma função deve ser igual ao número de chamadas para a outra. **MAPIInitialize** retornará S_OK se o MAPI não tiver sido inicializado anteriormente. 
  
Um cliente ou provedor de serviços deve chamar **MAPIInitialize** antes de fazer qualquer outra chamada MAPI. Se isso não fizer, as chamadas do cliente ou do provedor de serviços retornarão o MAPI_E_NOT_INITIALIZED valor. 
  
Ao chamar **MAPIInitialize** de um aplicativo multithreaded, de definir [](mapiinit_0.md) o parâmetro _lpMapiInit_ como uma estrutura MAPIINIT_0 que é declarada da seguinte forma: 
  
 **MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
e chame: 
  
 **MAPIInitialize** ( &amp; MAPIINIT); 
  
Quando essa estrutura é declarada, o MAPI cria um thread separado para manipular a janela de notificação, que continua até que a contagem de referência de inicialização cai para zero. Um serviço do Windows deve definir o membro **lags** da estrutura **MAPIINIT_0** apontado por  _lpMapiInit_ como MAPI_NT_SERVICE. 
  
> [!NOTE]
> Você não pode chamar **MAPIInitialize** ou **MAPIUninitialize** de dentro de uma função **DllMain** Win32 ou qualquer outra função que crie ou termine threads. Para obter mais informações, [consulte Usando objetos Thread-Safe dados.](using-thread-safe-objects.md) 
  
 **MAPIInitialize** não retorna nenhuma informação de erro estendida. Ao contrário da maioria das outras chamadas MAPI, os significados de seus valores de retorno são estritamente definidos para corresponder à etapa específica da inicialização que falhou: 
  
1. Verifica parâmetros e sinalizadores.
    
    MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS. O chamador passou um parâmetro ou sinalizador inválido.
    
2. Inicializa as chaves do Registro exigidas pelo MAPI e confirma o tipo de sistema operacional. Essa etapa só acontece se o processo do cliente estiver sendo executado como um serviço no Windows e define o sinalizador MAPI_NT SERVICE na **estrutura MAPIINIT_0** configuração. 
    
    MAPI_E_TOO_COMPLEX. O processo de chamada é um serviço do Windows e as chaves do Registro exigidas pelo MAPI não puderam ser inicializadas. 
    
    Informações adicionais podem estar disponíveis no log de eventos do aplicativo.
    
3. Verifique a compatibilidade de MAPI com OLE e inicialize o OLE.
    
1. Verifica se há compatibilidade entre as versões atuais do OLE e MAPI. 
    
    MAPI_E_VERSION. A versão do OLE instalada na estação de trabalho não é compatível com esta versão do MAPI.
    
2. Inicializa o OLE. 
    
    Somente durante esta etapa, essa função pode retornar um código de erro não listado aqui. Qualquer erro  _não_ listado aqui deve ser assumido como vindo da função OLE **CoInitialize**.
    
4. Inicializa variáveis globais por processo.
    
    MAPI_E_SESSION_LIMIT. O MAPI configura um contexto específico para o processo atual. As falhas podem ocorrer no Win16 se o número de processos exceder um determinado número ou em qualquer sistema se a memória disponível estiver esgotado.
    
5. Inicializa variáveis globais compartilhadas de todos os processos.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Não havia recursos suficientes do sistema disponíveis para concluir a operação.
    
6. Inicializa o mecanismo de notificação, cria sua janela e seu thread, se solicitado pelo MAPI_MULTITHREAD_NOTIFICATIONS sinalizador. 
    
    MAPI_E_INVALID_OBJECT. Pode falhar se os recursos do sistema se esgotarem. 
    
7. Carrega e inicializa o provedor de perfil. Verifica se **MAPIInitialize** pode acessar a chave do Registro onde os dados de perfil estão armazenados. 
    
    MAPI_E_NOT_INITIALIZED. O provedor de perfil encontrou um erro. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI usa o **método MAPIInitialize** para inicializar MAPI em um thread em segundo plano para fazer alguns processamentos de tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

