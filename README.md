class Schedule:
    def __init__(self, year, month, caregivers):
        self.month = month 
        self.caregivers = caregivers
        self.schedule = defaultdict(lambda: {"AM": None, "PM": None})