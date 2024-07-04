# Script-e-mail
Esse script é referente ao meu e-mail de previsão diário feito em HTML, pois o servidor que utilizo para envio permite o anexo de HTML e me da mais liberdade para criação de layouts e alteração de cores. Está já é a versão 2.0 do Script, última atualização sofrida no dia 04 de junho de 2024.

```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Previsão</title>
    <style>
        /* Variáveis CSS para cores */
        :root {
            --fundo: #15202b; /* Cor de fundo escura */
            --texto-claro: #FFFFFF; /* Texto claro */
            --texto-escuro: #000000; /* Texto escuro */
        }

        /* Estilos base */
        body {
        background-color: var(--fundo);
        color: var(--texto-claro);
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        }

	.alert-vermelho {
	background-color: #FF0000; /* Vermelho */
	color: #FFFFFF; /* Branco */
	padding: 10px;
	border: 1px solid #CC0000; /* Vermelho escuro */
	}
	.alert-laranja {
	background-color: #FFA500; /* Laranja */
	color: #000000; /* Preto */
	padding: 10px;
	border: 1px solid #CC8400; /* Laranja escuro */
	}
	.alert-amarelo {
	background-color: #FFFF00; /* Amarelo */
	color: #000000; /* Preto */
	padding: 10px;
	border: 1px solid #CCCC00; /* Amarelo escuro */
	}
	.alert-verde {
	background-color: #90EE90; /* Verde */
	color: #000000; /* Preto */
	padding: 10px;
	border: 1px solid #008000; /* Verde escuro */
	}

        h1, p {
        margin: 0 0 10px;
        }

        section {
        padding: 1px;
        margin: 10px 0;
        }

        footer {
        background-color: var(--fundo);
        color: var(--texto-claro);
        padding: 5px;
        line-height: 0.5; /* Altere o valor conforme necessário */
        font-size: 12px;
        text-align: center;
        }
        .text_1 {
        padding: 3px;
        margin: 10px 0;
        line-height: 1.2; /* Altere o valor conforme necessário */
        font-size: 11px;
        }
        
        .banner {
        width: 100%;
        height: 110px;
        display: block;
        object-fit: cover;
        margin: 0 auto;
        }

        @media only screen and (min-width: 767px) {
            .mobile-banner {
                display: none;
            }
        }

        /* Layout responsivo */
        .container {
        max-width: auto;
        width: 96%;
        padding: 10px;
        background: #FFFFFF1A;
        border-radius: 10px;
        box-shadow: 0 0 10px #0000001A;
        margin: 10px auto;
        }

        @media (prefers-color-scheme: dark) {
            .container {
                background: #000000CC;
                box-shadow: 0 0 10px #FFFFFF1A;
            }
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
        border: 1px solid #dddddd;
        text-align: center;
        padding: 8px;
        }
        th {
        background-color: var(--cabecalho-escuro);
        color: var(--texto-claro);
        }
    </style>
</head>
<body>
    <div class="container">
        
        <a target="_blank" href="https://cdn.star.nesdis.noaa.gov/GOES16/ABI/SECTOR/ssa/GEOCOLOR/3600x2160.jpg">
            <img class="banner desktop-banner" src="https://cdn.star.nesdis.noaa.gov/GOES16/ABI/SECTOR/ssa/GEOCOLOR/900x540.jpg?timestamp=000000048"> <!-- ##### NÃO ESQUECER DE ALTERAR ##### -->
        </a>

        <section>
            <p>Boa tade!</p>
            <p>Com prazer, apresento mais um dia do meu serviço de previsão meteorológica para Santa Maria e região próxima.</p>
        </section>
        
        <section>
            <h2>Previsão - Segunda-feira, 24 de junho</h2>
            <p>Tivemos chuva nas primeiras horas da madrugada, com nebulosidade intensa no período da manhã e o sol aparecendo entre nuvens no início da tarde. Para o fim da tarde e início da noite, não há previsão de chuva. As temperaturas para hoje são de máxima de 17°C e mínima de 10°C.</p>
        </section>
        
        <section>
            <h2>Previsão - Terça-feira, 25 de junho</h2>
            <p>O sol deve brilhar ao longo da manhã, com uma tarde de sol entre nuvens. Para a noite, está prevista chuva. As temperaturas para esse dia serão de máxima de 14°C e mínima de 7°C.</p>
        </section>
        
        <section>
            <h2>Previsão do tempo para os próximos dias</h2>
            <table>
                <thead>
                    <tr>
                        <th>🗓️ Dia</th>
                        <th>🌂️ Previsão</th>
                        <th>🌡️ Temp. Máx.</th>
                        <th>🌡️ Temp. Mín.</th>
                        <th>⚠️ Alerta</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- Linha para Hoje -->
                    <tr>
                        <td>Hoje</td>
                        <td>🌥️</td>
                        <td>17°C</td>
                        <td>10°C</td>
                        <td class="alert-verde">-</td>
                    </tr>
                    <!-- Linha para Amanhã -->
                    <tr>
                        <td>Ter. 25/06</td>
                        <td>🌤️🌧️</td>
                        <td>14°C</td>
                        <td>7°C</td>
                        <td class="alert-verde">-</td>
                    </tr>
                    <!-- Linha para 2 dias no futuro -->
                    <tr>
                        <td>Qua. 26/06</td>
                        <td>🌧️☁️</td>
                        <td>14°C</td>
                        <td>7°C</td>
                        <td class="alert-verde">-</td>
                    </tr>
                    <!-- Linha para 3 dias no futuro -->
                    <tr>
                        <td>Qui. 27/06</td>
                        <td>☀️</td>
                        <td>17°C</td>
                        <td>6°C</td>
                        <td class="alert-verde">-</td>
                    </tr>
                    <!-- Linha para 4 dias no futuro -->
                    <tr>
                        <td>Sex. 28/06</td>
                        <td>☀️</td>
                        <td>16°C</td>
                        <td>8°C</td>
                        <td class="alert-verde">-</td>
                    </tr>
                </tbody>
            </table>
            <div class="text_1">
            <p><i>*Previsão valida somente para Santa Maria–RS e região próxima, em um raio médio de 100 km.</i></p>
            <p><i>**Todo dia a tabela segue sendo atualizada, a medida que o resultado dos modelos meteorológicos são atualizados diariamente e analisados.</i></p>
            </div>
        </section>

	<section>
            <p>- Grau de evento severo no alerta:</p>
            <table>
                <thead> <!-- Cabeçalho da tabela -->
                    <tr> <!-- Linha do cabeçalho -->
                        <th>Intensidade</th>
                        <th>Nível de Alerta</th>
                    </tr>
                </thead>
                <tbody> <!-- Corpo da tabela -->
                    <tr> <!-- Linha do corpo -->
                        <td class="alert-verde">Sem Perigo</td>
                        <td>Nenhum perigo meteorológico. Condições meteorológicas estáveis.</td>
                    </tr>
                    <tr>
                        <td class="alert-amarelo">Perigo Potencial</td> 
                          <td>Condições meteorológicas que podem trazer riscos, como chuvas intensas, ventos fortes ou outros fenômenos meteorológicos que requerem atenção.</td>
                    </tr>
                    <tr>
                        <td class="alert-laranja">Perigo</td>
                          <td>Condições meteorológicas perigosas. Fenômenos meteorológicos que podem causar danos significativos ou perigo à vida.</td>
                    </tr>
                    <tr>
                        <td class="alert-vermelho">Grande Perigo</td>
                          <td>Condições meteorológicas extremamente perigosas. Fenômenos meteorológicos que podem causar desastres severos e representar grande perigo à vida.</td>
                    </tr>
                </tbody>
            </table>
        </section>

<section>
    <h2>Climatologia:</h2>
	<p>Para o mês de junho, registramos um total de 236,1 mm de chuva, de acordo com os dados obtidos da estação convencional do INMET de Santa Maria. Esse volume corresponde a 177,92% da média de chuva esperada para o mês, conforme a série climatológica (1991-2020), que é de 132,7 mm.</p>   
	<p>Barra de progresso referente ao volume acumulado comparado ao esperado para o mês:</p>

	<div style="height: 20px; border: 2px solid #ccc; border-radius: 5px; background-color: #f0f0f0; width: 285px; margin: 0 auto; position: relative;">
    	<div style="height: 100%; border-radius: 1px; background-color: #4caf50; width: 177.92%;">
    	<span style="margin: auto; top: 50%; left: 50%; transform: translate(-50%, -50%); color: black; font-size: 12px;">177.92%</span>
</div>
	</div>

            <!--<div class="text_1">
            <p> *Dado de precipitação correspondente das 09 horas, do dia anterior dessa previsão, devido à leitura do dia atual só ser efetivada no sistema após as 12 horas.</p>
            </div>-->
</section>

        <section>
            <h2>Satélite:</h2>
            <p>- Imagens de satélite das últimas 4 horas:</p>
            <img src="https://ciram.epagri.sc.gov.br/ciram_arquivos/meteorologia/satelite/animation.gif?timestamp=0000048" width="517.5" height="450" alt="últimas imagens de satélite"> <!-- ##### NÃO ESQUECER DE ALTERAR ##### -->

            <h2>Modelo:</h2>
            <p>- Imagem de modelo meteorológico do total de chuva prevista para o acumulado de 24h do dia atual:</p>
            <img src="https://sigmameteorologia.com/produtos/wrf_ecmwf//wrf_chuva_acum_rs_24h_00z_25.png?timestamp=000048" width="568.2" height="365.4" alt="últimas imagens de satélite"> <!-- ##### NÃO ESQUECER DE ALTERAR ##### -->
            <p>Para facilitar a compreensão, a imagem mostra o valor que é esperado de chuva ao longo das 24 horas do dia.</p>
        </section>

        <div class="text_1">
            <p><b>OBS:</b></p>
            <p>- Meu intuito é trazer a previsão de forma simplificada e compreensível a todos, tendo alta assertividade. Caso deseje dar algum feedback ou viu algum erro, retorne para o e-mail <a href="mailto:suporte@mmeteologia.com.br?subject=FeedBack%20previs%C3%A3o">suporte@mmeteologia.com.br</a>.</p>
            <p>- O banner no topo do escopo desse e-mail é a imagem de satélite do último minuto, e se clicar sobre, será aberta no site da fonte em tela cheia e alta resolução.</p>
            <p>- Valores de referência utilizados com base no Instituto Nacional de Meteorologia (INMET), Defesa Civil e Organização Meteorológica Mundial (OMM ou WMO).</p>
            <p>- Caso deseje realizar uma doação, utilize nossa chave Pix: <a href="https://link.mercadopago.com.br/gruporebelo">pix@mmeteorologia.com.br</a>. Ao clicar sobre a chave, você será redirecionado para mais opções de pagamento, como boleto, cartão de crédito, débito, entre outros.</p>
        </div>
    </div>
    
    <footer>
        <p>&#169; M.Meteorologia | Developed by Mateus Rebelo | 2024 | Todos os direitos reservados.</p>
    </footer>
</body>
</html>
```
