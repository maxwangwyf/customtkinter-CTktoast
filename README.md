 def show_toast(message, duration=1000):#toast窗口
        toast = ctk.CTkToplevel(fg_color=main_col)
        toast.geometry(f"200x80+{w//2}+{h//2}")
        toast.overrideredirect(True)  # 隐藏标题栏和边框
        toast.attributes("-topmost", True)  # 窗口置顶
        label = ctk.CTkLabel(toast, text=message,font=('微软雅黑',20),fg_color='#14375E',text_color='white',corner_radius=10)
        label.place(relx=0, rely=0, relwidth=1, relheight=1)
        toast.after(duration, toast.destroy) 
