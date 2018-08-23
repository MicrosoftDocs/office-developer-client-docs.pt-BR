---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9f37e57f997ead58b1ef0e9a27ccbdb0a810be06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571952"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aloca e inicializa um objeto OLE **IStream** para acessar o conteúdo de um arquivo. Essa função usa uma sequência de caracteres ANSI, como o nome de arquivo, incluindo o caminho e a extensão de arquivo, portanto, o uso da versão Unicode dessa função, [OpenStreamOnFileW](openstreamonfilew.md), é recomendado.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parâmetros

 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores usados para controlar a criação ou a abertura do arquivo a ser acessado através do objeto OLE **IStream** . Sinalizadores a seguir podem ser definidos: 
    
SOF_UNIQUEFILENAME 
  
> Um arquivo temporário deve ser criada para o objeto **IStream** . Se esse sinalizador estiver definido, os sinalizadores STGM_CREATE e STGM_READWRITE também devem ser definidos. 
    
STGM_CREATE 
  
> O arquivo deve ser criada, mesmo se já existir. Se o parâmetro _lpszFileName_ não estiver definido, esse sinalizador e o STGM_DELETEONRELEASE devem ser definida. Se STGM_CREATE for definido, o sinalizador STGM_READWRITE também deve ser definido. 
    
STGM_DELETEONRELEASE 
  
> O arquivo deve ser excluído quando o objeto **IStream** for lançado. Se o parâmetro _lpszFileName_ não estiver definido, esse sinalizador e o STGM_CREATE devem ser definida. 
    
STGM_READ 
  
> O arquivo deve ser criada ou aberta com acesso somente leitura. 
    
STGM_READWRITE 
  
> O arquivo deve ser criado ou aberto com permissão de leitura/gravação. Se esse sinalizador não estiver definida, o sinalizador STGM_CREATE não deve ser definido uma. 
    
 _lpszFileName_
  
> [in] O nome de arquivo, incluindo o caminho e a extensão, do arquivo para o qual **OpenStreamOnFile** inicializa o objeto **IStream** . Se o sinalizador SOF_UNIQUEFILENAME estiver definido, _lpszFileName_ contém o caminho para o diretório no qual deseja criar um arquivo temporário. Se _lpszFileName_ for NULL, **OpenStreamOnFile** obtém um caminho adequado do sistema e os STGM_CREATE STGM_DELETEONRELEASE sinalizadores e devem ser definidos. 
    
 _lpszPrefix_
  
> [in] O prefixo para o nome de arquivo no qual **OpenStreamOnFile** inicializa o objeto **IStream** . Se definido, o prefixo deve conter não mais de três caracteres. Se _lpszPrefix_ for NULL, um prefixo de "SOF" é usado. 
    
 _lppStream_
  
> [out] Ponteiro para um ponteiro para um objeto expondo a interface **IStream** . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_NO_ACCESS 
  
> O arquivo não pôde ser acessado devido a permissões insuficientes do usuário ou porque os arquivos somente leitura não podem ser modificados. 
    
E_NOT_FOUND 
  
> O arquivo designado não existe.
    
## <a name="remarks"></a>Comentários

A função **OpenStreamOnFile** tem dois usos importantes, diferenciados pela definição do sinalizador SOF_UNIQUEFILENAME. Quando esse sinalizador não estiver definida, **OpenStreamOnFile** abre um objeto **IStream** em um arquivo existente, por exemplo, para copiar o conteúdo à propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo usando o **IStream :: CopyTo** método. Nesse caso, o parâmetro _lpszFileName_ Especifica o caminho e o nome do arquivo. 
  
Quando SOF_UNIQUEFILENAME estiver definido, **OpenStreamOnFile** cria um arquivo temporário para armazenar dados para um objeto **IStream** . Para este uso, o parâmetro _lpszFileName_ opcionalmente pode designar o caminho para o diretório onde o arquivo deve ser criada, e o parâmetro _lpszPrefix_ , opcionalmente, pode especificar um prefixo para o nome de arquivo. 
  
Quando o aplicativo de cliente chamada ou o provedor de serviço for concluído com o objeto **IStream** , ele deve liberá-la ao chamar o método OLE **IStream::Release** . 
  
O MAPI usa as funções apontadas pela _lpAllocateBuffer_ e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação, especificamente para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp:: GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O sinalizador SOF_UNIQUEFILENAME é usado para criar um arquivo temporário com um nome exclusivo para o sistema de mensagens. Se esse sinalizador estiver definido, a parâmetro de _lpszFileName_ Especifica o caminho para o arquivo temporário e o parâmetro _lpszPrefix_ contém os caracteres de prefixo do nome de arquivo. É o nome de arquivo criado <prefix>HHHH. TMP, onde HHHH é um número hexadecimal. Se _lpszFileName_ for NULL, o arquivo será criado no diretório atual ou o diretório de arquivo temporário que é retornado da função Windows **GetTempPath**se nenhuma diretório de arquivos temporários foi designado. 
  
Se o sinalizador SOF_UNIQUEFILENAME não estiver definido, _lpszPrefix_ será ignorado e _lpszFileName_ deve conter o caminho totalmente qualificado e o nome do arquivo a ser aberto ou criado. O arquivo será aberto ou criado com base em outros sinalizadores que são definidos na _ulFlags_. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|CPP  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI usa o método **OpenStreamOnFile** para abrir um stream em um arquivo, de forma que um anexo pode ser gravado em-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

