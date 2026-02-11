import discord
from discord.ext import commands
import random


intents = discord.Intents.default()
intents.message_content = True
start = 8
characters = ["Reciclar materiais","se puder, jogar lixos orgânicos em composteiras","jogar lixo no lixo","Reutilizar","fazer uma horta"]
char = random.choice(characters)

bot = commands.Bot(command_prefix="!", intents=intents)

# ================= READY =================
@bot.event
async def on_ready():
    print("Bot ligado como", bot.user)
# ================= COMANDOS =================

@bot.command()
async def oi(ctx):
    await ctx.send("Olá! Diga '!comandos' para acessar todos os comandos disponíveis para conversar com o Box")

@bot.command()
async def  obrigado(ctx):
    await ctx.send("Fico muito feliz com isso 😄")

@bot.command()
async def  tchau(ctx):
    await ctx.send("Até mais😉📦👋")

@bot.command()
async def  comandos(ctx):
    await ctx.send("comandos:")
    await ctx.send("!combustiveis")
    await ctx.send("!dicas")
    await ctx.send("!problemas")
    await ctx.send("!obrigado")
    await ctx.send("!tchau")
    await ctx.send("!oi")
    await ctx.send("Ps:não se esqueça de sempre colocar uma '!' após cada fala para acessar o bot")

@bot.command()
async def combustiveis(ctx):
    await ctx.send("Combustiveis:")
    await ctx.send("Os combustiveis são a nossa principal fonte de energia para carros,casas,etc..")
    await ctx.send("Eles são separados em dois tipos,renováveis e fósseis.")
    await ctx.send("Os combustiveis renovaveis são fontes de energia produzidas a partir de matérias-primas orgânicas (biomassa), como plantas e resíduos, ou fontes naturais inesgotáveis (solar, eólica, hidrogênio). Eles se regeneram em curto prazo, oferecendo alternativas sustentáveis aos combustíveis fósseis,")
    await ctx.send("além de serem uma fonte de energia mais 'limpa',poluindo menos o meio ambiente.")
    await ctx.send("As energias renováveis mais famosas são:")
    await ctx.send("-Energia solar-")
    await ctx.send("-Energia eólica-")
    await ctx.send("-Energia hidrelétrica-")
    await ctx.send("Já os combustiveis fósseis são aqueles que poluem o mais meio ambiente além de terem um tempo de renovação mais lento,imperceptível pra escala humana podendo levar milhões de anos")
    await ctx.send("As energias fóssei mias famosas são:")
    await ctx.send("-Carvão-")
    await ctx.send("-Petróleo-")
    await ctx.send("Por que estou falando esse conteúdo?")
    await ctx.send("Porque se acabarmos utilizando bastante energia poluente podemos piorar o aquecimento global,e cada vez mais estamos caminhando para isso,e se não fizermos alguma coisajá pode ser tarde demais.")

@bot.command()
async def problemas(ctx):
    await ctx.send("Os principais problemas que podem acontecer se não soubermos pluir menos o meio ambiente são:")
    await ctx.send("Desmatamento florestal")
    await ctx.send("Secas")
    await ctx.send("Aquecimento global")
    await ctx.send("Extinção de espécies")
@bot.command()
async def dicas(ctx):
    char = random.choice(characters)
    await ctx.send("sua dica para ajudar o meio ambiente é:")
    await ctx.send(char)# meio-ambiente
