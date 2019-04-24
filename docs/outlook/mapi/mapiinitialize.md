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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346638"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Incrementa a contagem de referência do subsistema MAPI e inicializa dados globais para a DLL MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Parâmetros

 _lpMapiInit_
  
> no Ponteiro para uma estrutura [MAPIINIT_0](mapiinit_0.md) . O parâmetro _lpMapiInit_ pode ser definido como nulo. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O subsistema MAPI foi inicializado com êxito.
    
## <a name="remarks"></a>Comentários

A função **MAPIInitialize** incrementa a contagem de referência MAPI para o subsistema MAPI e a função [MAPIUninitialize](mapiuninitialize.md) decrementa a contagem de referência interna. Portanto, o número de chamadas para uma função deve ser igual ao número de chamadas para o outro. **MAPIInitialize** retornará S_OK se o MAPI não tiver sido inicializado anteriormente. 
  
Um cliente ou provedor de serviços deve chamar **MAPIInitialize** antes de fazer qualquer outra chamada MAPI. Se isso não for feito, as chamadas do cliente ou do provedor de serviços para retornar o valor MAPI_E_NOT_INITIALIZED. 
  
Ao chamar **MAPIInitialize** de um aplicativo multithread, defina o parâmetro _lpMapiInit_ para uma estrutura [MAPIINIT_0](mapiinit_0.md) que é declarada da seguinte maneira: 
  
 **MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
e ligue para: 
  
 **MAPIInitialize** (&amp;MAPIINIT); 
  
Quando essa estrutura é declarada, o MAPI cria um thread separado para manipular a janela de notificação, que continua até que a contagem de referência de inicialização fique como zero. Um serviço do Windows deve definir o membro **parâmetroulflags** da estrutura **MAPIINIT_0** indicada por _lpMapiInit_ como MAPI_NT_SERVICE. 
  
> [!NOTE]
> Você não pode chamar o **MAPIInitialize** ou o **MAPIUninitialize** de dentro de uma função **DllMain** do Win32 ou qualquer outra função que crie ou encerre threads. Para obter mais informações, consulte [usando objetos isentos de threads](using-thread-safe-objects.md). 
  
 **MAPIInitialize** não retorna informações de erro estendidas. Diferentemente da maioria das chamadas MAPI, os significados de seus valores de retorno são estritamente definidos para corresponder à etapa específica da inicialização que falhou: 
  
1. Verifica parâmetros e sinalizadores.
    
    MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS. O chamador recebeu um parâmetro ou sinalizador inválido.
    
2. Inicializa as chaves do registro exigidas pelo MAPI e confirma o tipo de sistema operacional. Esta etapa só ocorrerá se o processo de cliente estiver sendo executado como um serviço no Windows e define o sinalizador de serviço MAPI_NT na estrutura **MAPIINIT_0** . 
    
    MAPI_E_TOO_COMPLEX. O processo de chamada é um serviço do Windows e as chaves do Registro necessárias para o MAPI não pôde ser inicializado. 
    
    Informações adicionais podem estar disponíveis no log de eventos do aplicativo.
    
3. Verifique a compatibilidade de MAPI com OLE e, em seguida, inicialize OLE.
    
1. Verifica a compatibilidade entre as versões atuais de OLE e MAPI. 
    
    MAPI_E_VERSION. A versão do OLE instalada na estação de trabalho não é compatível com esta versão do MAPI.
    
2. Inicializa o OLE. 
    
    Somente durante esta etapa, essa função pode retornar um código de erro não listado aqui. Qualquer erro _não_ listado aqui deve ser considerado proveniente da função OLE CoInitialize ****.
    
4. Inicializa as variáveis globais por processo.
    
    MAPI_E_SESSION_LIMIT. O MAPI configura o contexto específico para o processo atual. Podem ocorrer falhas no Win16 se o número de processos exceder um determinado número ou em qualquer sistema, se a memória disponível estiver esgotada.
    
5. Inicializa variáveis globais compartilhadas de todos os processos.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Não há recursos de sistema suficientes disponíveis para concluir a operação.
    
6. Inicializa o mecanismo de notificação, cria sua janela e seu thread, se solicitado pelo sinalizador MAPI_MULTITHREAD_NOTIFICATIONS. 
    
    MAPI_E_INVALID_OBJECT. Pode falhar se os recursos do sistema estiverem esgotados. 
    
7. Carrega e inicializa o provedor de perfil. Verifica se o **MAPIInitialize** pode acessar a chave do registro onde os dados de perfil estão armazenados. 
    
    MAPI_E_NOT_INITIALIZED. O provedor de perfil encontrou um erro. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> ||MFCMAPI usa o método **MAPIInitialize** para inicializar o MAPI em um thread de plano de fundo para executar algum processamento de tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

