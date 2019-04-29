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
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439090"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aloca e inicializa um objeto de **IStream** OLE para acessar o conteúdo de um arquivo. Esta função usa uma cadeia de caracteres ANSI como o nome do arquivo, incluindo o caminho e a extensão do arquivo, portanto, o uso da versão Unicode dessa função, [OpenStreamOnFileW](openstreamonfilew.md), é recomendado.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
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
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
 _ulFlags_
  
> no Bitmask dos sinalizadores usados para controlar a criação ou a abertura do arquivo a ser acessado através do objeto OLE **IStream** . Os seguintes sinalizadores podem ser definidos: 
    
SOF_UNIQUEFILENAME 
  
> Um arquivo temporário deve ser criado para o objeto **IStream** . Se esse sinalizador estiver definido, os sinalizadores STGM_CREATE e STGM_READWRITE também deverão ser definidos. 
    
STGM_CREATE 
  
> O arquivo deve ser criado mesmo que já exista um. Se o parâmetro _lpszFileName_ não estiver definido, esse sinalizador e STGM_DELETEONRELEASE deverá ser definido. Se STGM_CREATE for definido, o sinalizador STGM_READWRITE também deverá ser definido. 
    
STGM_DELETEONRELEASE 
  
> O arquivo deve ser excluído quando o objeto **IStream** for liberado. Se o parâmetro _lpszFileName_ não estiver definido, esse sinalizador e STGM_CREATE deverá ser definido. 
    
STGM_READ 
  
> O arquivo deve ser criado ou aberto com acesso somente leitura. 
    
STGM_READWRITE 
  
> O arquivo deve ser criado ou aberto com permissão de leitura/gravação. Se esse sinalizador não for definido, o sinalizador STGM_CREATE não deverá ser definido como. 
    
 _lpszFileName_
  
> no O nome de arquivo, incluindo o caminho e a extensão, do arquivo para o qual o **OpenStreamOnFile** Inicializa o objeto **IStream** . Se o sinalizador SOF_UNIQUEFILENAME estiver definido, _lpszFileName_ conterá o caminho para o diretório no qual criar um arquivo temporário. Se _lpszFileName_ for nulo, **OpenStreamOnFile** obterá um caminho apropriado do sistema, e os sinalizadores STGM_CREATE e STGM_DELETEONRELEASE deverão ser definidos. 
    
 _lpszPrefix_
  
> no O prefixo para o nome de arquivo no qual o **OpenStreamOnFile** Inicializa o objeto **IStream** . Se definido, o prefixo deve conter não mais de três caracteres. Se _lpszPrefix_ for NULL, será usado um prefixo de "SOF". 
    
 _lppStream_
  
> bota Ponteiro para um ponteiro para um objeto que expõe a interface de **IStream** . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_NO_ACCESS 
  
> O arquivo não pôde ser acessado devido a permissões de usuário insuficientes ou porque arquivos somente leitura não podem ser modificados. 
    
MAPI_E_NOT_FOUND 
  
> O arquivo designado não existe.
    
## <a name="remarks"></a>Comentários

A função **OpenStreamOnFile** tem dois usos importantes, distinguidos pela configuração do sinalizador SOF_UNIQUEFILENAME. Quando esse sinalizador não é definido, **OpenStreamOnFile** abre um objeto **IStream** em um arquivo existente, por exemplo, para copiar seu conteúdo para a propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo usando o **IStream :: Método CopyTo** . Nesse caso, o parâmetro _lpszFileName_ especifica o caminho e o nome do arquivo. 
  
Quando SOF_UNIQUEFILENAME é definido, o **OpenStreamOnFile** cria um arquivo temporário para armazenar dados de um objeto **IStream** . Para esse uso, o parâmetro _lpszFileName_ pode opcionalmente designar o caminho para o diretório onde o arquivo deve ser criado, e o parâmetro _lpszPrefix_ pode opcionalmente especificar um prefixo para o nome do arquivo. 
  
Quando o aplicativo cliente ou provedor de serviços de chamada é concluído com o objeto **IStream** , ele deve liberá-lo chamando o método OLE **IStream:: Release** . 
  
MAPI usa as funções apontadas por _lpAllocateBuffer_ e _lpFreeBuffer_ para a maioria da alocação e desalocação de memória, em particular para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto como [IMAPIProp:: ](imapiprop-getprops.md)GetProps e [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O sinalizador SOF_UNIQUEFILENAME é usado para criar um arquivo temporário com um nome exclusivo para o sistema de mensagens. Se esse sinalizador estiver definido, o parâmetro _lpszFileName_ especifica o caminho para o arquivo temporário e o parâmetro _lpszPrefix_ contém os caracteres de prefixo do nome de arquivo. O nome de arquivo <prefix>construído é HHHH. TMP, onde HHHH é um número hexadecimal. Se _lpszFileName_ for nulo, o arquivo será criado no diretório de arquivos temporários que é retornado da função **GetTempPath**do Windows ou do diretório atual se nenhum diretório de arquivo temporário tiver sido designado. 
  
Se o sinalizador SOF_UNIQUEFILENAME não estiver definido, _lpszPrefix_ é ignorado e _lpszFileName_ deve conter o caminho totalmente qualificado e o nome do arquivo a ser aberto ou criado. O arquivo será aberto ou criado com base nos outros sinalizadores definidos no _parâmetroulflags_. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Arquivo. cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI usa o método **OpenStreamOnFile** para abrir um Stream em um arquivo para que um anexo possa ser gravado nele.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

