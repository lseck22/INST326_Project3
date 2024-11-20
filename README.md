class Schedule:
    def __init__(self, year, month, caregivers):
        self.month = month 
        self.caregivers = caregivers
        self.schedule = defaultdict(lambda: {"AM": None, "PM": None})

def display_schedule(self):
        num_days = calendar.monthrange(self.year, self.month)[1]
        
        # Begin the HTML calendar layout
        html = f"<h2>Schedule for {calendar.month_name[self.month]}</h2>"
        html += "<table border='1' style='border-collapse: collapse; width: 100%;'>"
        html += "<tr><th>Day</th><th>AM Shift</th><th>PM Shift</th></tr>"
        
        for day in range(1, num_days + 1):
            am = self.schedule[day]["AM"] or "Unassigned"
            pm = self.schedule[day]["PM"] or "Unassigned"
            html += f"<tr><td>{day}</td><td>{am}</td><td>{pm}</td></tr>"
        
        html += "</table>"