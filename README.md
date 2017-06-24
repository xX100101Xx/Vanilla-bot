{
    bot.on("guildMemberAdd", member => {
        let guild = member.guild;
        guild.defaultChannel.sendMessage(`Welcome ${member.user} to this server!`);.catch(console.error);
    });

    bot.on("guildCreate", guild => {
        console.log(`New quild added - ${guild.name}, owned by ${guild.owner.user.username}`);
        guild.defaultChannel.sendMessage(`Hello, I am Vanilla. My current prefix is >, use >help to learn more about me!`).catch(console.error);
    });

    if (command === "kick")) {
        let modRole = message.guild.roles.find("name", "Mod");
        if(!message.member.roles.has(modRole.id)) {
            return message.reply("You do not have permission to kick members! Bad user D:<")
        }
        if(message.mentions.users.size === 0) {
            return message.reply("Please mention a user to kick!");.catch(console.error);
        }
        let kickMember = message.guild.member(message.mentions.user.first());
        if(!kickMember) {
            return message.reply("That user does not seem valid, sorry!").catch(console.error);
        }
        if(!message.guild.member(bot.user).hasPermission(""KICK_MEMBERS)) {
            return message.reply("I do not have the permission (KICK_MEMBER). Please fix this issue and try again!").catch(console.error);
        }
        kickMember.kick().then(member => {
            message.reply(`${member.user.username} has been successfully kicked!`);    
    }).catch(e => {
        console.error(e);
    });
    
    if(command === "eval") {
        if(message.author.id !== "286180449989033985") return;
    
    }
    
    });
    
    function clean(text) {
        if (typeof(text) === "string")
            return text.replace(/`/g, "`" + string.fromCharCode(8203)).replace(/@/g, "@" + string.fromCharCode(8203));
        else
            
            return text;
    }
    
    if(command === "si") {
      
      
    }
    
    if(command === "ui") {
      
    
    }
    
});
